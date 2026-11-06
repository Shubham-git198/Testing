<!--<header>-->
<!--    <div class="header-inner">-->
<!--        <div class="hdr-left">-->
<!--            <div style="font-size:15px;font-weight:700;color:var(--text2)">Process Aro Pump · Vibration Monitor</div>-->
<!--        </div>-->
<!--        <div class="hdr-right">-->
<!--            <div class="pill pill-g" id="machinePill">-->
<!--                <div class="dot dot-g"></div><span id="machineLabel">SENSOR ONLINE</span>-->
<!--            </div>-->
<!--            <div class="clk" id="clk">--:--:--</div>-->
<!--        </div>-->
<!--    </div>-->
<!--</header>-->

<!--<main>-->

    <!-- KPI ROW -->
<!--    <div class="sec">KEY PERFORMANCE INDICATORS</div>-->
<!--    <div class="kpi-row">-->
<!--        <div class="kpi" style="--ka:#0ea5e9;animation-delay:.04s">-->
<!--            <div class="kpi-lbl">X — RMS Velocity</div>-->
<!--            <div class="kpi-val" style="color:#0284c7" id="k-xv">—</div>-->
<!--            <div class="kpi-unit">mm/s RMS</div>-->
<!--            <div class="kpi-d st" id="k-xvd">loading…</div>-->
<!--        </div>-->
<!--        <div class="kpi" style="--ka:#6366f1;animation-delay:.08s">-->
<!--            <div class="kpi-lbl">Y — RMS Velocity</div>-->
<!--            <div class="kpi-val" style="color:#4f46e5" id="k-yv">—</div>-->
<!--            <div class="kpi-unit">mm/s RMS</div>-->
<!--            <div class="kpi-d st" id="k-yvd">loading…</div>-->
<!--        </div>-->
<!--        <div class="kpi" style="--ka:#10b981;animation-delay:.12s">-->
<!--            <div class="kpi-lbl">Z — RMS Velocity</div>-->
<!--            <div class="kpi-val" style="color:#059669" id="k-zv">—</div>-->
<!--            <div class="kpi-unit">mm/s RMS</div>-->
<!--            <div class="kpi-d st" id="k-zvd">loading…</div>-->
<!--        </div>-->
<!--        <div class="kpi" style="--ka:#f59e0b;animation-delay:.16s">-->
<!--            <div class="kpi-lbl">Peak Acceleration (HF)</div>-->
<!--            <div class="kpi-val" style="color:#d97706" id="k-pk">—</div>-->
<!--            <div class="kpi-unit">G PEAK</div>-->
<!--            <div class="kpi-d st" id="k-pkd">X / Y / Z</div>-->
<!--        </div>-->
<!--        <div class="kpi" style="--ka:#ec4899;animation-delay:.20s">-->
<!--            <div class="kpi-lbl">Temperature</div>-->
<!--            <div class="kpi-val" style="color:#db2777" id="k-tmp">—</div>-->
<!--            <div class="kpi-unit">°C INTERNAL</div>-->
<!--            <div class="kpi-d st">WARN: 85°C | CRIT: 100°C</div>-->
<!--        </div>-->
<!--        <div class="kpi" style="--ka:#10b981;animation-delay:.24s">-->
<!--            <div class="kpi-lbl">Machine Status</div>-->
<!--            <div class="kpi-val" style="color:#94a3b8;font-size:15px;padding-top:5px" id="k-ms">NO DATA</div>-->
<!--            <div class="kpi-unit" id="k-noise">Acc Mag: — G</div>-->
<!--            <div class="kpi-d st">Motor_Run_Flag</div>-->
<!--        </div>-->
<!--    </div>-->

    <!-- WAVEFORM + LEVELS + PREDICTION -->
<!--    <div class="sec">VIBRATION HISTORY &amp; ACCELERATION LEVELS</div>-->
<!--    <div class="g-main">-->

        <!-- Velocity history (Plotly) -->
<!--        <div class="card">-->
<!--            <div class="card-t">Velocity Trend <span class="badge b-live">LIVE</span></div>-->
<!--            <div class="card-s">RMS velocity · last 60 samples (5 h at 5-min interval) · selected axis</div>-->
<!--            <div class="atabs" id="wtabs">-->
<!--                <button class="atab ax" onclick="setWAxis('x',this)">X-AXIS</button>-->
<!--                <button class="atab" onclick="setWAxis('y',this)">Y-AXIS</button>-->
<!--            </div>-->
<!--            <div id="waveChart" style="height:160px;"></div>-->
<!--        </div>-->

        <!-- Acceleration levels (Plotly bar) -->
<!--        <div class="card">-->
<!--            <div class="card-t">Acceleration Levels <span class="badge b-ok">G</span></div>-->
<!--            <div class="card-s">Full-band RMS · high-freq RMS · high-freq peak · selected axis · hover for peak frequency</div>-->
<!--            <div class="atabs" id="stabs">-->
<!--                <button class="atab ax" onclick="setSAxis('x',this)">X-AXIS</button>-->
<!--                <button class="atab" onclick="setSAxis('y',this)">Y-AXIS</button>-->
<!--            </div>-->
<!--            <div id="specChart" style="height:160px;"></div>-->
<!--        </div>-->

        <!-- Fault indicators -->
<!--        <div class="pred-card">-->
<!--            <div class="card-t">Fault Indicators <span class="badge b-ml">HEURISTIC</span></div>-->
<!--            <div class="card-s">Hover each indicator for calculation breakdown</div>-->
<!--            <div class="rul-box">-->
<!--                <div class="rul-val" id="rulV">—</div>-->
<!--                <div class="rul-lbl">HOURS REMAINING USEFUL LIFE (ESTIMATE)</div>-->
<!--                <div class="rul-sub" id="rulSub">Estimate only</div>-->
<!--            </div>-->
<!--            <div class="fault-list" id="faultL"></div>-->
<!--            <div class="pred-info" id="pCD">Waiting for data…</div>-->
<!--        </div>-->

<!--    </div>-->

    <!-- HEALTH + TEMP + EVENTS -->
<!--    <div class="sec">DIAGNOSTICS</div>-->
<!--    <div class="g-bot">-->

        <!-- Health ring + gauges -->
<!--        <div class="card">-->
<!--            <div class="card-t">Machine Health Score <span class="badge b-warn">WATCH</span></div>-->
<!--            <div class="card-s">Overall vibration severity · ISO 10816 style · from worst-axis RMS velocity</div>-->
<!--            <div class="ring-wrap">-->
<!--                <div class="ring-rel">-->
<!--                    <canvas id="ringC" width="130" height="130"></canvas>-->
<!--                    <div class="ring-inner">-->
<!--                        <div class="ring-score" id="hScore">—</div>-->
<!--                        <div class="ring-txt">HEALTH %</div>-->
<!--                    </div>-->
<!--                </div>-->
<!--                <div class="gauge-row">-->
<!--                    <div class="g-item">-->
<!--                        <div class="g-val" style="color:#0284c7" id="gX">—</div>-->
<!--                        <div class="g-track"><div class="g-fill" id="gXf" style="width:0%;background:#0ea5e9"></div></div>-->
<!--                        <div class="g-lbl">X mm/s</div>-->
<!--                    </div>-->
<!--                    <div class="g-item">-->
<!--                        <div class="g-val" style="color:#4f46e5" id="gY">—</div>-->
<!--                        <div class="g-track"><div class="g-fill" id="gYf" style="width:0%;background:#6366f1"></div></div>-->
<!--                        <div class="g-lbl">Y mm/s</div>-->
<!--                    </div>-->
<!--                    <div class="g-item">-->
<!--                        <div class="g-val" style="color:#059669" id="gZ">—</div>-->
<!--                        <div class="g-track"><div class="g-fill" id="gZf" style="width:0%;background:#10b981"></div></div>-->
<!--                        <div class="g-lbl">Z mm/s</div>-->
<!--                    </div>-->
<!--                </div>-->
<!--            </div>-->
<!--        </div>-->

        <!-- Temp & vibration magnitude -->
<!--        <div class="card">-->
<!--            <div class="card-t">Temperature &amp; Vibration Magnitude</div>-->
<!--            <div class="card-s">Temperature_C &amp; Magnitude_XYZ_HighFreq_RMSAcc_G · latest values</div>-->
<!--            <div style="display:flex;align-items:baseline;gap:6px;margin:6px 0 2px">-->
<!--                <div class="temp-big" id="tmpV">—</div>-->
<!--                <div style="font-size:18px;color:var(--muted)">°C</div>-->
<!--            </div>-->
<!--            <div style="font-size:9px;color:var(--muted2);font-family:'Space Mono',monospace;margin-bottom:14px">-->
<!--                WARN: 85°C &nbsp;|&nbsp; CRITICAL: 100°C-->
<!--            </div>-->
<!--            <div style="font-size:10px;font-weight:700;margin-bottom:6px;color:var(--text2)">-->
<!--                HIGH-FREQ ACCELERATION MAGNITUDE</div>-->
<!--            <div style="font-size:26px;font-weight:700;color:#059669;margin-bottom:6px" id="noiseV">— G</div>-->
<!--            <div class="noise-bar">-->
<!--                <div class="noise-pin" id="noisePin" style="left:0%"></div>-->
<!--            </div>-->
<!--            <div style="display:flex;justify-content:space-between;font-size:8px;color:var(--muted);font-family:'Space Mono',monospace">-->
<!--                <span>0 G</span><span>1 G</span><span>2 G</span>-->
<!--            </div>-->
<!--            <div style="font-size:10px;font-weight:700;margin-top:14px;margin-bottom:5px;color:var(--text2)">-->
<!--                TEMP TREND (LAST 2 H)</div>-->
<!--            <div class="spark-row" id="sparkR"></div>-->
<!--        </div>-->

        <!-- Events -->
<!--        <div class="card">-->
<!--            <div class="card-t">System Events</div>-->
<!--            <div class="card-s">Event log</div>-->
<!--            <div style="font-size:10px;font-weight:700;margin-bottom:6px;color:var(--text2)">-->
<!--                RECENT EVENTS</div>-->
<!--            <div class="ev-log" id="evLog"></div>-->
<!--        </div>-->

<!--    </div>-->

    <!-- TREND (Plotly) -->
<!--    <div class="sec">RMS VELOCITY TREND</div>-->
<!--    <div class="card" style="margin-bottom:24px;">-->
<!--        <div class="card-t">-->
<!--            RMS Velocity — All Axes (Xaxis / Yaxis _RMSVel_mm_sec)-->
<!--            <div style="display:flex;gap:14px;font-size:10px;font-family:'Space Mono',monospace;">-->
<!--                <span style="color:#0284c7">— X</span>-->
<!--                <span style="color:#4f46e5">— Y</span>-->
<!--            </div>-->
<!--        </div>-->
<!--        <div class="card-s">Stored history from telemetry (5-min samples) · hover for exact values</div>-->
<!--        <div id="trendChart" style="height:220px;"></div>-->
<!--    </div>-->

    <!-- DETAIL CHARTS (Plotly) -->
<!--    <div class="sec">WAVEFORM SHAPE STATISTICS</div>-->
<!--    <div style="display:grid;grid-template-columns:1fr 1fr;gap:14px;margin-bottom:24px;">-->
<!--        <div class="card">-->
<!--            <div class="card-t">Crest Factor — Full-band vs High-freq</div>-->
<!--            <div class="card-s">*_CrestFactor · latest snapshot · per axis</div>-->
<!--            <div id="harmAclChart" style="height:200px;"></div>-->
<!--        </div>-->
<!--        <div class="card">-->
<!--            <div class="card-t">Kurtosis — Full-band vs High-freq</div>-->
<!--            <div class="card-s">*_Kurtosis · latest snapshot · per axis (above ~3 suggests impacts)</div>-->
<!--            <div id="harmVelChart" style="height:200px;"></div>-->
<!--        </div>-->
<!--    </div>-->

<!--</main>-->

<!--<footer>-->
<!--    <span>Predictive Vibration Monitoring</span>-->
<!--    <span id="lastSync">Last data: —</span>-->
<!--    <span>DEVICE: Process Aro Pump</span>-->
<!--</footer>-->

<!-- Rich Fault Tooltip -->
<!--<div class="ftip" id="faultTip">-->
<!--    <div class="ft-head">-->
<!--        <div class="ft-htitle" id="ft-title">—</div>-->
<!--        <div class="ft-hsub" id="ft-sub">—</div>-->
<!--    </div>-->
<!--    <div class="ft-body">-->
<!--        <div class="ft-sec">-->
<!--            <div class="ft-sec-t">Detection Algorithm</div>-->
<!--            <div class="ft-formula" id="ft-formula">—</div>-->
<!--        </div>-->
<!--        <div class="ft-sec">-->
<!--            <div class="ft-sec-t">Feature Contributions</div>-->
<!--            <div id="ft-features"></div>-->
<!--        </div>-->
<!--        <div class="ft-sec">-->
<!--            <div class="ft-sec-t">Per-Axis Score</div>-->
<!--            <div id="ft-confidence"></div>-->
<!--        </div>-->
<!--    </div>-->
<!--    <div class="ft-foot" id="ft-foot">—</div>-->
<!--</div>-->

<!--<div class="stip" id="stip"></div>-->
<header>
    <div class="header-inner">
 <div class="logo">
      <div class="logo-icon">
          <!--MI-->
          <img style="width:100%" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAPoAAACLCAYAAABIkoRZAABlLklEQVR42ux9B3wc9ZV/7nKpgG21VZeBkAq21cuquYEhJISUfyq5dAJc7kIIqaSQI7lcSDnSSCchIY1eEzo2GONeZUlWl7YXafvO7szufP/vvZld7SqSLRybYu/w+bGytLsz85vf973ve79XXoLCUTgKxwl/vKQwBYWjcBSAXjgKR+EoAL1wFI7CUQB64SgchaMA9MJROApHAeiFo3AUjgLQC0fhKBwFoBeOwlE4CkAvHIWjAPTCUTgKRwHohaNwFI4C0AtH4SgcBaAXjsUeuq7LeLbvyfzucL9f6LsX857DXcdi3184CkAvHOaRTqdlHOnvc9+zmN8/m/c8m2td7PsLRwHoJweIoWeHnvn3XG2opqBF4vxHIJWGlohD1eh9Gv2bRiyZRDStgn4LLUnfkGLVyn+jHzSN3qciqqpQ05lzsOY1fkjpaRkCTPosVF2+k78iSW9K0ed0+jxSKWQ/TH9PwARyMoVESoVC743SPxV6v0LfpfCb+fuSGlJ0DXypSfqdIt+cywBmr4VunP5qXGPhKAD9hAU6DwEeASVLgWnxp5M6AVgXAKcZ6Kkk4vSqpFOEsySBXoEWmoFmm4I+Mobkrv0IP/IUErfci+kf/h7O626E40vfw8SV38Lw5V/DwIe/gMEPfQFDH/wchi/5rIyRS67G1Ie+DNuHr4Ht41/F1Oe/A9uXvw/v//0O0T/cDTz6NLQ9B5AaGQVcDmDaT0IhRqJFQUJPQNM1ub6UStef0kVeJPl6SUYgwcKE7o2EhZ57b7oh1ESwpWf/XQB6AegnNNA1ArlG4FVTWpb+phjMCulKXwCRhzbB/fM/oO/yL2Fj41ux5Q3nYXddL4aLWuE8rRmhVzfCVtoGd1kHApYuDFU2YbSyBeNVLRitoNeKVkzSGKtsxUR5CyYtzbBXt8lwVrbBV9QCf3ErfCWtmCqj99N7xssaMVrehJHqFtjK2mCztMNRYYWzqgvjxc2YpPMNWDqxva4Hj7xhPTae92GMXfYNKN/8NSJ/fQipXX1AIAD4I0glVcS0ZM69pUlIqDLojrOALxwFoL+4j0RKtFoiQQQ2oYqmg0lzVaK48WSU3hJF0mVD5MGn4L7mBzh47ofQ/8YLMFzeiaHSdoQqVyOyrAXTS1YiUN4KRxmBt2QFvDUE2tKV8JZ3wE3DWd4Ob2kLZgiY0wRQd2kH/b0dUwRMZ0UnbBUdBPoOTFk6YCu3wk6/myyjUWrFRJkVU5X0fv4u+p2nrB0eOpedBISDBIXD0oKp8mbY6N/2ajpPCZ2DhEO4qAnhpSRESptJOJCQoL8dXNKIA0UkDFach/4Nl2D00i9i6s93YHqEBECCBECI2ECI7pkpPjN9mp84Czq2IFIFO78A9BfAMZ9neqHB9qlm2p/EtmEYrSkoMzOA04/gvU9gzxXfwM6zNuCZmjbsPb0DY8vbYVvehvE60sjVDThQvQqDdaRdzyRtXGfFWK0VfRVtOFTejYGaNdhGmnZLdReees1qPH7Oemxf92HYSLtGvvEzovB/hHLTPdD/8jD0R54BNu4AntmL5L5BaAcOQdt/CPreg0jv6UOaqD+e2I7UQ09D/9ND0H5xF5Trf4fE5d/AaNd7sbXKisermum1HfurOrGzphu7LXSdtT04dFY7Riz1cL/iTbAV1WO0pgUTp62ErbadhEkrvJVWuIqt6F/SQEykBU9f8DFM3nwXMOYCSToEVSXre0BIW9TcFo4C0I8v7V7Aez3fUElTJdnjFCdNHkkgcsfD+FP7W7DtNedhqMQKf3UPnCXNpKHb4a7qQZA0uJe08HRFN2aWtiFUshpTNetw56veiPvPOQ+uG26C8ugm6OPjCIdniAkkEIgG6btp4ccIAHE6bzJBdrMmNj3LljiNGF94KuORk5uY9YilWI2mjVfT6aaYn4nTPxLsF+SP03vUdEKGRudVgyHAPQ3sHYRy6/3wXfVdTLZ9GHsr2xEgUI+T5g+U0P0sa4J96QpMlNST1m8gZtFKAqEVQ8Qg9hED2XX2hXhk7SVIPX2AtHsSIXb5LWJuC0cB6McP4Ow0E8zo4ojif6XSKv+fKGkSCqkllVAR1wlkMT9iA4MYv/J/0F/eC8cpjRinhT5cXY+Zqiai1fXwETUOEsX1FhNltvSgr3IN9r/uAgx2fgAT1/wUoa39hneLPelEadmpxWaAppHWy2hA7bnbx46I800nm5u97MxOSAGTYEkS8BFwYeRzXycbvx0TZ3QiROaFh7T3dHkX2fh037UtZPO3wVfcClddJ3xFDUjSe+2WZoyRyTBe04k9Lz0Hw5dcDWXrfoTpxmIkvDQ6UVohgaMSP2JvXzyNgueuAPTjrsnFU0ygixPlZHNSpaH4QrKFlGZ+TuCeuuyr2PgvZ8NXuxpuotaj1U0YWt6I0cqVcFQ2kI1MNvZr12IbLfyn2t6B/Z/6KrBtH32RQt+jYjThQzAeRyxI2lkzwJ02PddpE+wqCZ3MOJ5Al10Bc6hRVcgAs4SwnkJCITv78W04cPHV2HlqC8b4vpZ3YH/52WSvryCbvgNOSxcCBGR2Ajqre0WTB+i9U8VNcJQ3Epuph7Ocfi5ugL2khQRfJ83ZBXjkJSsx/fM/I0Jmzoye4L09xGh+2HmXKiC9APTjCXTeBovTMouRZgvrRHBpsacmXfDf8Efsbn4vhk5hT3YL+mrqMVXWCDdR2GDletiqVmO0qBsHOz4Az2e+i8gjTwP+AClqVWz4RCINLcnbUmkkVbLhWWMTNUgn4kgyS6DzsHdeN30EhsDhjW9VxvEEOl2FmB881GQECAZhv+1BbF33IQy9oglKEVHx0hbsrmhD34c/jci138X0qe2IEG0freqG752Xw33hBxAm82QXaXjc9hCCu3bA9s2fYE/LxdhDWt1Z3Q0HmS6BpSQYKrvgqmlH3+lNmKhtQn9xJ7a9/s2YfvQpqJEwmUMJiRMoHAWgH52T7TC/VwnYSkKR/e1IJIYkUenoPRux7x3/gX7SUBO00P0WArWlg2ztbthPayZK2oE9RMn3EA23/e42YN84UV2CDWulZ2HnLzT+GXAfKQw2LcEybB6kxM5Xg3Gkd45i6hNfx77T12JwKdnbVa1QK3qxq2QVhq74DPTtO+D62g8wWGOFf3k3+sg2d9/wK7i/egMGq5rhIEEw9P6rESIanjE/hBLtH8HkVddjD33Gf0ozDp7RDqWiG64l9QiREHCQeeOkOXaXrcXus94K991/h6KGyFzgLbq0OBAy87GQs7QA9MJB62TWKTXfIuFgFXZGOZUgafIEpu56ELta3w4/ATpQQdqodAXR8Wa4Le04eOoqHCSqvvfCy4AHdpEBGxO7lr8g44VPP0vP/fHwQB/uuxg0YdHgKeLoccQfehIbmy+GvbgHh+rWwV7XCw9vs53SigOrP4CE34l4Xx+2tFwE5/J1sFU0YeDVjQg/vQ+eJ57GSHk3xovegKEqK1J+v2yhzZ7PwHoskUCEwDvyvd9gqPxCDFZaEarpJQG6Ap6SRgJ6G8bLOEaAND5994j1IrjuuIvYvAIPafhc06YA9ALQ5z9Spodcn19zcoAHghH4v38zdp++AVNL2uGr6sSIpQUeopkTpHH2LV2FXfUXwvbjX5NE8CDJjrm4LlvmalKiWWkYYab6MXIYHyug/8P9ctjrhAvj37sJzzS8DQNkY9sqWjFctwIu3kM/rRVPrXsfwtv2I0rCb/IHv8dA6WoozGzOWoP9ZKKEH9qE5IAXfdXnYnx5G7w87roPkXgYejKWvQ4OFJKAIS1N35WARiMVjWDmljux9Yw1su9vq2yAg+x7b1k3QkUdGK6oh8uyCpPFrdi59qPQ904JOzgc2AtALxyyOHixsQ3Kll+K0KmbIZyRVATjN9yMx2o64alZA1e1FZ6Xv0ki0bYTwLcR6Ps/di1wYAK0ihFKRqHQd3EMuGKC6IW00HQJSU0bEetk94ejQSNwJ60gHiIB1X8Qo+/9DNnFrfCVWhE+jWxqeh0mYLnO6sKu1/ci8eRT0AIRBEMzGP7AlxEtPx9jRSQEltVjrPodwPYpmjoVf1/7HviW98C+rBmD534COkf6kXkdgSYRcf8gbzOhwCxoUmQqRAKY/u4fsYVMovBZG4j6nwNvNdntxSsxVdOKAIF+uoyAf2Ynon+5E8l0DKF43HimMQK+kpJdEq0QR18AOh8McN624r1k8WJrCmZoOSbGx2A7tQvelzfAWdSIqdpWDL6mFYeWrsTE0i7Ef3I7lGiI3qsjntYEMOkUb7fpsi2tpfGCBHqaLowUqSSjhFQF8o8d+3F760VwV5MwK2omwK7E9orXYbK2AeG6tdhR3IXQE8/QfSYRCvqBrQex97R2RGrXwH5WPYG9CZs6LoTq8MBDAJv4y98QL+qCSqxnU3UjcHDE2B8nOKvq/EA3TBvS7PSesKaLuZMUm8mHPZ/8IqaL2sXROV5F5605T3YuDp3RCE/FGxAo78GmprcDNgcCiRCC/P1yaykRHgWNfhI62/4BdqphKCZJw3njQaQG+rFjxVsxWNOB6DKijtWdmChpQIgW9dhpRCF/+FtasikJgGEnHdv4yRTvq9Pa0k1qbo4XCtCNOBljW4r3owV0ewax591XYfhV7XCVr8bAWb3wLmuFm7e5LG1EmXuxsf1tGH7kCcxEwhJwk/T48eC574Ot1grfKxsQJTo9cOZajH79B9CjYSS0BGbufRCDROXdpzVgf+kqzFz/K7L56Yhy+I1ixuT845yI5mWBS3ZOgl4DadV0hMYRVkLQh+3YvfqDcJ7SAnsdmRCWJniJWY1XtMn1DtG/R+mZ9V15DZKRaTMVLyU+lpNdp59UQOdoL90MCMs7eIuWNVsoQCD+JXYTsGMVq3Ho1HMwXdcsWzwHy9tw6FPXIuV0C8iDvOm0QJRWygx71Z7DxTXXHs0NwTXRQpSYblRVod33DHaseicmSOP2ldP9WXgrsB4B9qRXt2Kgsh1PV3TB/+tbRfvqpKGVRBieO+7D3rIeBJatxlhxCyZrmiTQZfRbvwSCKjwsSA4ME/B7ESlro+/qxP71HxKThoMNjiT0FrSpxZ4ynHZQ4tj7/R9jrLQT/spu7KNrmClpIjOjFR4a9rIW+Eq68GTru4ARG/EyVQJ8cnJiT0rb/SQDOlNrptX5DqioRnBwTmLjxf+OodPbML2kEY7qdgwTuOOkKeyvPxfh+x8mm08RYSFrL5GUxbNQJZdsGubzAPSMoOG9dyXO10zMQwlg5oGH8dR5l8BZTNqbKXB1CxQCrK28BVMVDJAWDFZ1wnnV/yLkcENTSP+y8zCZRN+nv45BMl9sVV1wlrXDS68OAtbIh69ELKYiTsIgFQhhR/d7Sdu2wVXZgAHStNi4nf6uiIA9aqCbgXASBMiezXAUoc27sWXV+UDxWkyWN8JJNN5L1xMobsNMpRUTdD/bXmsF9vRLhJ2a5oSZlIwC0E94Y9wAepRBYHpo02Sf6v5pPHbWWqRf3Qk324G0QINlq+DmffA3XigeaCWlQEuJ20pAxLZkegGN/XwsJDmflhLhwpawSvfFkXoM9PCf/oZNrz0fzldximoLPK8jsL7yHBJiHdhf2wh7UQtGCeQ72t6MqGsMCSVBtnESMxz/Zrdh97uvQLhkDWn+FgTKmjG1ZCVcZa1wnfcfCCXcpK05A03D/g9+FoeWkxlATIiz3cas76friAtCVfwTQEc2BB+xdNTwqXAW4NA4tlvfBSdp93FiIjYCd6iIrot+dpW3I/RvTXjw9euhPrOPhHtSwK5zQY6cSMIC0E9I97qRqJEmY5oDQJjWYdKJvlVvRbi4m+zxVjhqrHCc3ksLdRX6yfaEz49oOv2Cc6rNBUacwZ1QJGJMarlEAxj+3P9i2+lEtWvXY7S6Q/LTnaS9PaVNRNUbEKjpQX9xEx4m6qvdfj/0oNuIwAslECat6Xl8MwaqSWNWkgAkLS6RfqTVg2Vd6P/A5UjGQpLwQieG5zu/wkBRM4GObHuau2j5eij79opNrur6PxWPP/dzGUEb1OjsPi929VwCHzETb1077JXEJliYlTFLaYKTbPaJciuif3uYBFcSsayAP7kcdCcV0FXT78ZA5y2e0Jat2PoqWvAlpH0qGjFV1QxPJTvgOvHY6d1I7ToIH2ukBF7wQE8RyDWGu9eOyR/9Fn3ETPzlpLktKxCt7YCTM8fI9nYRYGd4W6p0HTYTiPs+8XUpEBFOhRGLh5BUEpKcs+fz38bkqd0YrWqHjWPUSYNPVFvRV2WF8+L/RFwLkiLXJGTXcc/fMVm1BmHOkbc0wF3eiqfpu0MM83RKWJSuH3ugsx0V4bjhMTf2VHcR2JsxsmwVJqqMohsO0vDse+gnwbO/thvBex6ma0pl4yYKQH+xe9fn2KuZoWhEu6MqQmoEwV/fiqElbRhc8nqMVHdikmxyP9FSL4H+sbaLiK77DW9tOv28OdXSmYi9nN8p6YTE1mlSyCIpmaVI0N/u2YhNrzkXU5Ye+Fj7EqgnSLs5KnsRLbaSEOPMsQaMLm/E06etgnrbg2TKKGLGxDWjZpwaJZp/+4PYbyEqXNVGgGmjOWnHWF2nFK8Yt1gRuvEPJE6CBPC42L4YcGAXF7Gg9/pKGkibdsJXfh6UwXF4+H5ShoF9LGdQRybT1thL4D1728NPYrpkLcbrmuU5ekir20nQuYnB+EgAzdR14WB1G9y//H0m4S9bry4z1y9EYV4A+mLBkjMUkv6JBFmwj2zGTqJ18ep1UOvOI/vOSjZdGyLFrdhHFDC+Zz9pfD0vpvz5BLqe4zxk75jORSM5Fj0Whffev2HH2edjrKYT0wRyd0mXeJ85PnyishUDxURnSXiFyGY+WN2Cobd8BKGgC1z1LcpSImoEqahqDFP3PojJV5PdXlFP4GAK3CpOrrHKBkwss2L0RzchmYwjRefWo6T5gwFsefOl8NeuhZ3ANUPnmKpZjQPrPkqaNiEx8sdz/jLfKxFxdE0H3vpJccT5iIH4+NrLSegR4F10XSNndWJmWTP2LmuHtn8IIS5nxQ7VAtBPDKBLYLU5kgmi4UMOPFHM+7C0cMuasKe0XqQ+O94mq2gxXPsTxKNcwfQFIKRMoEvQhznYwZaKh4FN23Bf/QakStbBQTZ3oKobY6/rxVh1K/wEbAYph60GljRioqgFOxs3IPGXR2XXgLPh5AcOBWC1Fgxi6H1XYaSoCyHeTz+jTUpE8ZYVf88wfU/4mz+TUliIpSVtNkk6cd/lX4eDgM3e7iBp/smiFdhR1Up287TQdXF+PkdATyhJ+LbvwPhSMi0qiJmJkOqRZ8uOQdtp9cQ6WnGowoqtaz4se/p6QaOfQEDn9cbEnWiqPuPG7hUXwVbXg6nyBgRLGjFSR7Y554dXdGFXx9uQnPYjKkUent97kHxrLqWqqHCxd4Er1Pij0MjO3N72DoyfSou3sgMTNR1w0KIer+ikeyD7u7SF7O8m+C2cbNOOvcXnwPO578IXibLyJiFGpoueMmJJVKLuThvuO3s9vFWrCRQEVqkXZ4Wnppeo70oSGh3Y/tHP02WEZT89rtLnyXxQfvNHTJb1SjHJ8JKVGKP5jJX2wvHf30dCjUvQi1SvPY7gUdNJ3jgEV+BIJlNIRmL4W/v/g72Ga90Re1neKfXvHFJPz4qRGtbyzbC/ciUif/grgpwCnEn/zTA/s2BnAegvMqDzg5TYaj2J0S99C+NE5+xE06cqyZYrIYpX2izOo2nSZh5avGmNFg3RQHbYPa/Xz/v7pHl9ySgQjsD38KPY3PsOjFTRwl3SBDe9ioeZ7sVjofshTeUoN4s5chHHsm4cbH831IeeJls5YRSk5KhSEmIRKRUdx8yf7sGO6rVQaNhPOwcjpxMIuOILV4ghIeGnsfOijyIdDUrF1jin6NLn1P196K/qFBuYzzld2ggvp6WWd0MdGiANawQT6cc5MlAq5cIIcdUTuqQOH/zWTzHOpgtrb650a7HKGKsiIUhMzkdCkBNkttVfQO9P0H2lsoU7civzFoD+IgN6TPaUCeg2F/ZY6CFXcV4zL2iyPWkxzJBd7ia7bdeqDdCmQ8b2i8YaT3verl2SbLiCDGvGbfuw/Yx1GD6lEdHqLvQTAxnnbaOiVgK4sefPgPdYOomidtA9NRM97cLBb/6Q7OgIIlzXKkJEO61KnLnEtU8H4bzqO3Av6cTYcisBopEA24QwMYQps0x0kMC/g6PL/EEj35t9A1Gyae0uHGi/GN4SMndIUHK9u0O8bUfgGrru/+jatecM6BJiLOaHLolI3EAi8vQOmqsWKVs1Ts87A3QWXj5iOy66z9HTWzBZ2gmM2wtAP3G87ip0WujbP/hpcSxlBgM9M3zVvfDccpc4j4y0i2PnJp5rc+ctJFNzs0aKJeNSMSaqRQiI0zj0PzfiKQK0jTU4gTl73ZVNYn8ysFlLsXfdVcSJHd1wLOvA7jXvxMyeQ1DjCuJcfSaWMqL5YgqUKA2bA9teY8VgreGwmyHAemnxT7GXnb5rlLS6l0Du/PfrEFfCSCkJROl71HgMutuNsbWXYKikns7Nde7aMFlRj9G6VuypIw0ZNbYin6sjvwinJp1j/JNTmKpeTffTgHEya6YqDGHOc8jsh4evuAnDJQ1w/uDXJBxUaBEj0OhEjpg78W30KEn5A8MYf9nKPKDnDq5vjpFxqf0mOelmcYjjCXTV3AtmjRLiEydUxBJBTHzl+xhcQuZEdQeiRIXdxc2itTPXKqDnIbXYGqS6Ktda380BMdf9AGo4IADnDLAk10knUySicdkrurcn92DzEjJTiMLKd5UbDrupKo4kaxUTYLpsDZ55y8fpemKkKUn0xY2wNq6IN3L5dXJ+z7KzMU2vY7UdcJU1on9ZI6bveFDs/jDSz5NAZ+quQZlw0D2ReUZa+1BJ47xAn6bhJiG5Y90HSMAq7AZBLK0VgP5iBjonn+z76OcxcUp9HrjdZbNjguzbdMwvVVUz++bqcQZ6KqeaK9wBTNxyOw6UdsN/1pthr+lG5LRmTJScI3HojjzB1InJKmNfPEC2+HhpG55uOB/KEzuNmO44O6aSJDQUcShy1lZSDWD6ht9gP2vt4gb4lm8QgE9y55Yqpv5sArSIA2v4nZ+nxR8juZOASsInrOvi9PL95HeYWNpKdLgFtjOtcJRYJezUS6DpP/eDwEyI2Ig4AZ6XZ65J77o0PJt2wlHWjcGKs+Gs6ZoX6AEuS0Xmzj00v0nPjOywpNLpAtBffEdKbDc+IskQtlV2wf/Sc/KAnnnoPKbquklxRRHXjQCPYwn0rH6TRoKQGHumDmxScDno4C13YvvyXgFOP8eJE5CmiU7z63zsY6SsA5GlXQgWG97k/g9eBdXlNUpCJ9NmUE1aGiVqzNnDEQxe+jm4ihvhK2uQLi6eUqK0xGLYgefh7ixE/SP0emjFeqh0TWTYwydubSPPXvXZMUxa31tEgqeiWRgQx5X7K7grzBoE7nv0edmayiSfcpUaPZ4kQRfD0NXfI7ZjlTTaYOlquldjTqXuXIbBVXbCzz6F16yF5nJIIU5eMAWgvwiBnqk1oNjH4FjaiUhl18JAr+5EKi6R77LVYpQ3PnZA183CaMlEQug0whqCtz6Mvtp1GOG8bqLdE0TDp5cSEMt4URrZZPOaGtxGqW4t9pSRjf5f35bAF+7dwCaA2Kq8+ImLJlnS2R14fO17kSxZB39ZG/ymAGEtx8UbOBw2vJRs1opebD57A5IH92Kay1Hohq+Cg4u4oaLtU9dimj37ZPeyI9Ndyg7NFnHgHXztBnpz/HkHOu/ZQ0ugr+cj0jvOVdpELIWfebvMZy7Qucqsl5jcEDGnxMiouBV0vaDRX3zUnXWybjQjmfn+LxC39GJfddOCQB8paYYyZRcb/Vg741KZCDsthfh0BGMf+CwGXtMBe1Wv9CqbqCbgFa2UsFUufDhR2SKeb9a88wE9sKQJ/dZ3AkMjUEmDpxKa2PfxTMJ22gD68I13EJi7SHu1IGqxSry6xLrTq7+0QQDPgxf8I70XA6NOhBkvSkK82EjFpFjm3k99DfaiDvi400rZijyNPkW2euCOO6RhxfMOdLqGmb2jsC9bg0M1xFCKGjBcZ3jbWWjac4FOrMhZxnn4nVD3D5B5lzJyEQtAf3Edqtmmlyn41PmfEMfVaHnzgs44T5EVroeeEFstebRAZybA1WbSKqJx0tyBmGjXqBZG2ufE5LU/xOO17bAta4KfFuB8/gJO/eQFydFonjIjv9rGDRVPWYXQmRuk19qeS78O+GYQjIeEfUhTBaadakpaFMfiMQT/+gAm6Z6c3P4o5zysyWXBS/IJ2a6WLuw/owcYdkhZqSRJugRNQpzs8+mZALy3PYoR3rbLMSNmCCDTNcRCaruxueNd9KGEmAzPT1SZ8YwT7HNVNez8yJcwXbl6ASY0K9jHLE0iAKeKO6UddCKhSY3AAtBfZIfQVjPsdetr1yNQ1SNOp4WAHiwhAF75bcnGOlrqns6UQWJbOZrGWDoEBGcw+rUfYXvNGniL2xF4ZZOAzV3atOC1ZICeBT07C19NQqr8PDhuuo2YdFDCT6NK3CxKJ+1HkSZ73K1HEbrul7DVrCXB1gFbab5wc+WcY6Sig6jrBqSCbtliQiRF7FczQoUjpM2dRPvPPo+EQbeAIyssylchQHavk+7J/qe74eHWUznVV58voCvEcIaKu3CwoumIQOeecHYS/PtK2gCHhwiR8dwKQH+xAV03AUAPcGttL3xFbZis6VgQXFOlK3HgzPOh+aeP3hmXNpgzL7pYMgr/136MPVWdcJV0wEvDwaWVKhvhLmnC5Bx2kbunnwF6Rsuzx/3AGesReWYr4hEFkXQS8aQCzayFlomFDydimCJtP7pkFQmTRvh4+43MgdzzZGLXRaudShR+eID4btK4ZmIhUTIAXGkCeYyo/9qPILi0BeM17WLnzl7rKjhK23D/63oQD5PQYU97Qn3egT604ZMYO6MTyaKOIwJ9orqNbPZmbCaBmwrHEGB/RCpRAPqL0Eg3wE5A3/6GCzFW0gLfqasWBPpkNYG9qBlTP/g5gShhtC9fTGQcN3YggRJNJBGlzwXZbNi+H4+91opo3VqyAZvElmVbmKOycsE8H9AdHMxRRfZvUaMIhkmyJXfX9kCZGCGmoYjPQSpQmmyFqypFOPXW68Ou918FR8VaTJ76RgnzZEebg2h3JkSWs9FsJfXwVPfgoKUD8fsfkohBxI38/Bhvw0nJaxVj3/gx7ETrXWSPc+aX0zKr0cfpOoer1yD12FMkYEjgEOdNPsdpvDL1Kdk7hF9LIPbkdgyVNGOwciXiy3oWfM5ZZsO14mletr37k0jHElJiDKbQlDz3AtBfPECX+qFEaafe/RnS5rTgX3H2gg/eXU3gqm7HBNnBODSOOGdD6ckjMwcSJDHZwSKaPuLA3os+iYklBGiyqUfqmuGuNZxq4umuXBjoLnM4ylqkuKGHrnespBGPdL1NChzG6W7CaaOho57O7b3OJw9i69s/STb9GjhOX4vholUSf258d1se0MfKW3Do1Hr4f3cHMYOIGRJrOC1ZfiTpB+/jT5CAIbCUc2XYDhnOHOruL+/Eo93vhBYKkWBQjTrszyEucoEeIfMlOTKCvqa3IFppODcnS9qPCHQGuYeEqOvm25Am214Ci0RwFID+4jrSRuSZeGN/8if0La1HYNnCdjFnbc1UkO1GgNjS837A5SOwJ6U+u6xiUaCGhzdjv3NwBmixK09uxeMr34zp5b20gFaKwHCXdUtu+HixodFt4vU1tnhmR5sMF53TXWqCqLgFo6WN2HumFeEvfYsMT6LpaloCebgZQUKTgF4BV+b8T7W+C75TSPtXNhNdt8JzGjGUik5J3OG4bq6d5uT9bgL6cFUXRv/zCxIEI9ZNJAovEfa0WSCVPe59xEQm60jwVDZJEQkBOhfIZIccXffe07uA3fsRIKrPOxSS+5M6/pJbN6MVNd0AZEpVYd++F/ssq+n+6oWOe4utsBfNpeyzwtReYVD4ca4mtKSJzJaghM5qSaOstKEgTsyWzCco0KVruaGxJh04sJRAVbOwhLdXcPRZOwJFVkzVrsEjPRcBg8NSpD0ATpowgKDHktwkzBj7D2F/y7vQ/6pGxGrXzYleW9zgyDT+nJ9sXi7ZZOdyxeU98D70ONK0+Nibnsr4G8zIulTCKDXNySXb1r0XzirS5BbrwjSVqDo3fQwVd2L8A1cDPp+wEAnegdGwIkVaTU1Gse+6GzC5rAMBYhQsOFhAyR50WZeUZRoprcfkVf8DJZ48dn2lFnNwlV6iM+I04/JV4QDcf7gHj71xA7wlvfBWWrPXmhtoJHvnJMDdHPLKhThqGuCgOedU3oH17xdBfiLnoJ/4QNcMe5MLJnIe+iMNF2CgcmGNzjXGbOUG0GOWNRgj0O8//Vx4r/ou4HRJQIgemgH2DcD181uwtfd9ZKuuxvjybvHyOmqtQrmPTBlnh4fLHXFFVQIUZ58ll3ZhBy3c4P4+SUAJkxrPBMHwFppulpTiPO+0bQqb172PbHGyo4mpOOoOQ1eruxAu6sHO+guRGB0lkMYQglmKSTey5OJR0s6bnkH/cisSy5iyN2KyimgwmxvsYyAB5CMbeMfKCxAj00bKZieTz53c1gwbWk8kiOEEMfq/P8ZQ9Vq4SHhFijskFoCfHwtrV47jkLU5h77aaH5tdD/uCu5N3yQtrKfveVTCXgtAf1EDXbZ2RXNFOFXzR7+D44w1QpXF6fUPHtkWCSbhNsfcz4s1bLRyHcZpce8sasHW156LPVU92LO0iYRCDwGhh2zVDsycugKeCgJE+cJCxGF60R3mPnYmxtxW3oAZssO9FlqARNn3E/VHOiiVX2xSaCItdqPRm1w3AmII5GG3Ew+3vxNK+TopGWWrJjAWrZz3nOy195ItOl6xBvGdW6V5g7Q3jJp9Swg8XFISMwo2Wd+NmbJV8J52DsYrV4oG53nhSL1pDpstJoH4xe9IcEycu5cm1eP7DHUjdp1ZTEw34hu04Aw2vuMyTJ/WIx1ZpkmTc3LKWGkDzSebGJxk0/EPQJ+i94xUcXmscwjsTXj6gg9BHBwpFID+ombuuemgyRQ0nxvbSq1EQXkrjYBVZf0HYDAAucYaO80ydvVkhVXCPf3FmQirdtJs7SY9NICQHQtp8Qoj+MVhOuG4zNN4VasUo7TT7/vJlt/c9i6i1B6pUKqZfdHYQWY4umjwPUyTHna7MXT22+Bavh6HiupJINE1VrKjbA51r2yXYJtwOdnYRUTDb/qzMQ9mlB47KWMM8LRKZkAcrm//ku6pB8MEdCcH1fA+s1nUgp1440tXYPdZa4Ax13MGjJg4DejeFU6RJVNp2oeDr3sLPMSkYhW98Jdl/B/tEqmXKfHsyWFWDtM299L8cP7A8Os78VhxPdS+AYRVEp/Jk6cS7AnqdZ+tnso1U+Nkf7r+cIc4lWa4ttkcYNrLZ7XglGnrudlTXm6Vsko+3gc348/Ziy4/VxqvRwK6y5K/N56p5eYngbGXrmfn+z4rxR2CTIX9SdKYSaTYC2za55KrHokgNDGC7ZW9mKFF7qzqhIOuw2069Vxlc4DOcegE9mFa1AfefSXUSIiotpHKKQyBu5VwpRk1isSOAxgjuj5MtDbMzjxLh0QSOiqMohYM9hDnA1zzA6kX91wBXU8aKbbcSGLkz3egnwSWr6gJfrr30YpmmXPxH3Asu8UqAM8K4FygMyuh9w8XnY2xVzQhfuOt9L0JYTaaEi8A/YRh8WnDmcWA2fX2K5Cw9ML32tVZwLlNbTs3eswAfhstljbxYOd6bh3lh7fFOS2S2QFrVc7z5n5mXHLYTvZ4vKgVo7Wr8eTpVgS3bEIiFZSIOqn0minvnDajb/hHJYbYnffDvqwLE0tWisaV81S052zTtcFvIbuaaDwDdaKyg0DRgUMfvYY0YUQiAtKqURtNgM6UIZFCwj2FvdXnCcX1VKySazX2zNuk3hzbtUMl5+CgpZuERThb/ebZAD0vNRd6fl+6tFG+OkmmALeqDCYThhBKcc25MGZ+eQt2VnRI9Rr2ljtMOu7Om2/jejPPc6qyNQv6MaLpE+UryfRoI7OrBaO3/AWJdFJsfkkLAApAP3GU+2zTQaHw1ndgcmmzVDm1m5TdaTm2g23w6WKz5DKBPFTcagC0pIls/WZ4a9+OxMZt4ukmuvEP4DGAn4ZPjyK2d580J3CVdsDNjRgWSF9lW58LSLCWDxV10X2+C5rTKVuMDOy0Zia9mCNAQJr8+DUYJnrPmtFT1pjHTLg7qbOsgcyANhxc/3EoKU6rjR090OdU5OXvkE2tOGluLuzIwUfszY/HMHP737Cv/b0YWcZsqm3R8+7IRhZmsvQ4gYedimsw9J0bwVEPUtEnPRt3VAD6CQj0eFqB3jeEvtpZje6yHHugZ76XFx0DL8jll+l3vjPWY+vKCxFyuqXqC/uDdC1fS8q2NFN21rqHRvHUyvMRPKVBkjA8S+rzqs3kOxTb5RwczTZ1qhXxjbukTpyiGt5xxewBz0OcfH97EuNlHcRQ6iUclPO2c4E+RT9PFzdioMaKyL2bEBAWkPynNHquSZXR8NxI2U9CB0oCiYlD2NT7Tsy8sh3u5WSmnNqA4dqmRc97JhHIbtJ6b0kz9tS2Yejz3yEhEjc69QQUiQJMpHU8T2UBC0A//h6elHQmCT+2FUOW9XBUdSBS2S37rEINK9ryEj8Ws7gyrCCbjCKjXQo1OiWxpAmJki4M0qL9e2039IBHgGYwdDPwJecIkNbk/mdRtxO7Xnsexqo7MVPSQJS8WexxW04AiCPn59GaZmgl3ZiydOHAldeS9o0Y5dvMBhBM28PSx50ETNiFHW+4EJOvWoGBijeZZoZ57+ZcBJcR1SX2sfM166AFQ0b/NNl3Tknu9mKiSnIr8ca4pptqtMUKcX08khvuNMFcCSP5wGPY0nkx+uvaZJ+bU2HZRzIpW4/N2WeRuWdbhomVz0b+8bNjau/l/IIyMouq1yFSugYj1/9YogeNnIC0sUPJ/g/TXCoA/QQ8mLKpMS6xlILrsSfRX9OFoao3ZZ1OLolWW7zmzjjxcqmj2PblraZ25X3sVgye3onHzuxCrO8gnAQ3Bps+pxhhZp88zIS2fwhb69+B0PINGFneRQu6UbSuIUTaso6m3PNOE0UdIqGwmSg7XE5EtVg2piVjW7Pnnc4O7xVfwTAJI3dFF3xLZlkNb/9l5iHEwOcSzhs+anRmEaGkS5VXXZfYQMw2R5rTNjr3P92IaJP66dyJNplEPEBXMTKG4c9/EyNnnA9bWQ/sxZl7NDzns9GEcwJgctN6y436eZk6eryjYuOc+yVGldehj1wl51QkmjCnlNdJtH9+UgJd43rmRD/5wSdCESQf3IJdp1ulAiprda7CMmXSbl/p4ih6pi8300YuH832uZEMYgxnaTeGzroI6rQPqmZ6gJL5AM8sPKHrdhceb7+YrqcHXvb6EzNwVDcLCHhx+wiA/Mrn9pZmdgpapZjkYHEXQEKC67Zz+ymJ384Beoq3lA4dwuipKxGwdGCMwBFdZpVrzzKSTAHFaq4uS5T+W78w9/DTZhGNXKBrOWP2kIg7M+pO4dp1zATY/p5JIviXx/C71rfDU0TzUrQSB2vaMGhplIIYUmPfdKRxXAMHwXAX10zWnVHjzjSJGOzlRjDMeLXx/DgZyEVm0oESK1w/vInjhjkcQUpjiWvABPrJ1jL5pAN6ngeYeCTnXeuOGeza8B5oZatJCzTCXkJgZ5rM++m0qHj4yxbeOmMtwwuwv874d6DYAOMoLb5RDsS58n8R1kLi9c6zxXM1OXcF5aqtB8hGLW7HUF0XohVWAfNchsGajuuui+YrNaqlzJD22lO5Fsoz2xGJBbLOLgYmx8frZLLE2Afn9WNL4/kYrzyyg8tVxh1UOxH/ye1GdldcR4AYgZopZEPfy1uXCtNyAn8sZfSD410CnXvQh4KIknAL3PoQhi68Ao+dUi9Zc65qK7yWJmO/e26Jp0UIVG7CwCWxpAIPzVGo2CqxCUP094MkHDaf/x5g0gOFBBPvWJ6MoC4APa/cspGImiIqz0kjj/a+HzNFvRJY4SW7cMDyJqGBPBwVbYvy+HpMTTtaUY/JJR1wf/uXxJajpMjCkhyzENAVlazpGR8erulGbGmvONZGi1fMC/Sx6hYpN8VAmS5rgJ1MgzEO473+FikBlTBiW7NAZxIR44quNCa/cyNGOQV2MeZJSaNkwfVd/hWoSTYDOKOPmIfCZbGM/G3xJmowGjwwG1FIYjndmPnT3di09hLSsGsIjKtln3vo1BUYL+H+Z01kErRKeO3h4g9yBwcYZRiM19T4TOltJQ2YpGcTOK0VT9S2I/qb2xBWQzTfEQS4ZEy6APSTHuj86ONplexPDal4WopFHPrS/2FnVTv8HOZayo0GO8n25e0n64LgzqXutgpjUfZXdcH/o5tJCSYEBHw2VVUX1uguHzZv+CASxCqcZEZ4CGSu8uZ5ge4sN0DOwTvj1U0Ilq/GMx/7tJRCUqQAhJ4H9AhpXkWNIbR5G/YzA6hsQqS0+chatLaNQNWMva9Zh+RT24iRhEhoxYgFJ+jnpLRcThN7SO85iOSv7sX29f+OTbU9GKxeizjdR/DVTeivrJe9bA5TDUn0GkcVdggdd1kWD3QpqUVzMVzTmg1WYmE3UdqBnUtbMHDhZYDHS88ziQixNPYlJFQj8aYA9JPR6z6PRzjXRuYRe2wLDtS/HYeW95JWbkKorAvDFUbl1ExkWyan3G0xPL6S7336OvGKDxR3YuxD30KII9Tjsbz+7Ehq2c1bVoAc7qoEnBh6z3+RfU9sgs7HwB6pNsyBTOhsXkBPFXcHbcREXTOGqogOv/5ipP1+SRmVQhicqKIbP3NSjxHKHsRgy/9bMB9+/u262ai/weVd2L/2/dh32TUY+MgXMLD+gxg4sxf7y5owSN81zv3lTT/HTGmbADETSpwf2NIhMelTFQtUgTGdou6MY9RsN+UvtWKYhB9725XiHgRKV2OMhPDBi/8DkYP90JOJvGeYOwpHAejzDg/z0UQMw1/6AQ7QApsi++/Q6R2yBeWas+1mNxcij7Glb8BUUQuG/+M6qKRVuB46N1HI09ya6XSjn2c4rj0aRt9/XUOg6EG4vBcuMhMkdbV8VqjMBQNH2I1XNSPICR2vbkF42x4EiTlkAC4178w2Twz+KAHe8Y1foP/ZBgblAH1s2UqEzzQ6rk5wfzdu9FC2kuz4Ntl/nybNKv3UTecYe8szIz+foIkEAicGzb837rbkAzzTdMHGiSvLGhGuXIu9y1qw+/JroPSNQKfn5NfiULT0gs+zcBSAPu9iSCdSYk/7EmHEhybwxJsuJK3VLR71rCYvm/X6Zob91A4MffGHkuetkN2fCMUN+zUnGkwqmLAA0FiYaBj74v+R3dqGyfJGTJU1YrS6JUtVc8+Vt6VHi57PN0xaf+KjXzb83YrReIKBnTbDZxUYoI/tGsHeIrKTKxvyutM8G6C7iltIU3fAe2qDOCanLTzayQwwWzmVteSBdP5kH0MouKSO3fw+DxYWGU86F5JgsHu5TVTluXi0hEyV//kZMO5EgjS47Cew95+9+rpWQHIB6EcnBBgwCncG1cjOnrBj/2VfRT83Y6QFf2A5LcoarkpDVNTShO1cH/1vm8QhJZ09U/mRbpkh9WG44Go4hL6rv0mf7cRUdddh01uFvhPllUy6MrJziTWME2UeePOHgekZo/SRmu9/iKa5SAPZqUEv7tnwHowUtUtGWm5gj/M5GI45RS+dFiPtlevn8c4Ba3wORXYsY3OkG/baXthIyMWXWZEoXY8HSxpw6DvfJ3D7kIxGoaZUI6pN2kQVtHUB6McI6HpSl1LIwXAQcalyEkfo8afwxMrz0FfXKyWjRitXI/rQ01KCOcHlp+IEZm0W6PkdVNMIkt0+eeOfMLK0VcpbeQ6jXTP0fbyyg0BhhbfEijgB/uAb1wLENjj3KkLXx9o89zzcWipBmm7ohl9iL7GFMGvT2ubnHOi59fAkIKeyRbztmYKZvEU2xVF/VZ3wlHdizNKFJ8ne33vNf0Oz2cn0CQvzYX3NdefjKV1qxXHmnezzFY4C0I8F0DPJD3GihmxX8z4xtzdmEHG9sYG7/o743j4p7aSmkhILrqZ0yZjLFjHM5JTTiJA694+OY8RyPoLcIabmHPgqmw/rbTYi8MgGLjH6fD9V1oz4A/djnANaExChYpTNmgU64yA5NIWddWsRqOoiFtIiJaafD6DnmgtGoomhzWWbkF6HljVjz6oLMPrN6xHftQspNQ5V06W6Dsfw8i4eZ5wxPY8rUSnaqXEGWipZWKgFoB9bOz5tVgfNDAa+gH8BT+/cdr68aHWFFmZQxZbXrYOb7HK3pUl6l01VNs06rzgXPhvSySWdOgmcnVJLbmZpG/pqSTh8/ptk5ysSXaeapaYy58xu32kx7H7n5fCUWPOAZquYpe9HttHb8tpWZYbbTNRxzw3kYdYgcebtCJU2w7ukEZ6lLeKw5Px4paIH4eLVOFTajY2cC/DvX4b3tr9D51JdhGglFpDIvdx7mc9zruU4HQtHAejH3GGX2SKTarBsg6cW9vTmDl6QCbL1OQTUu3kr7CXt2FXbYDi5zHTKDNCl4EWOg48ruLolK43AU9yLnRs+QsLCj2A6YbREzhEqDAhuwcyvkf4DGKrtIMbQNi+NXpRGXwDoRvUZc+TY35McTUgA9xQTc6izwlHTjUOnNmBPcSuerL8Q9iu+gcif7wMm7VDjIcQkrJaEFZk6TM1j3CUnlZo/ziDPW5rj3CwcBaAfV888Dl+0IPdzrHWVFAflJBDZtgf2L16HJ1/Xi4Nn9uAQl6cq7TC26biWXAXZ7KLJCehcvZSEAJeLGluyEk/Unw9Mh4wSS/E0wmoCuckkKTOuPRGL4eC6D0NZdg5R/8asFpdSWVXGmKyaPxnHbvZid1iM4g4eAXduQ0r2mreIJ9zPGWP0b1tFB4YJ4OMVa7G7ugcj1vfBff0voO/bD0WZJrodQ4i7u3LmmvgS6KqJkCjiMFTBOXZcfAJmGefCUQD6i9LOl/ryutFNNZAIE93n6ikRqRGH/cMI/v5+BK76PjYt78XGV74R48Wd8C/pQLKYGxJYMXImAYjobvyRJxFVIgueL55IIsZJO/c9hInieriXvEm0ros7p5qDC1l6S5vgL24gpsDtoVbBXbQS02T3+0saMV1Cf+OsNvYL1HTBS8D1FrVDeTUJpH9dRQKnA7v/rQmPEyXfv+7f4f3K/0F/4AnAZUc0yQ0dkkb/Nm5aSPfLRS9YS8tIzx/rXzgKQD8hgJ5tvqgZrX01RZN9bqOsky652Ym0inhKgRINQpl2Qxs8BM8DD2Pwhpuw/YprYb/xr5AyFfTZ1AJ54OwE5E6uO9/+CcyUdMNX2YMxC/dF780Ob+UastV74FpGdn9JF6aqejFZuxaj9Lv+ZR3Yf0oL+k7twkjdmzG4/pPY997PYuQbP8LkrXdDGRqCEvKTjIoQ3Y6RmZCEzmGmXOs+oEnMQCbXm1NSORPP6GhrjJSeLgC9APQTF+iymFMG0OPpTBVWlWirItRbSyYkuCUonUzFbCWqnzICYYiic+aZhyVEUocfWLDeQ5zAp4dIq//+YeDme5C+5X7glieBPz6YHfpdjwOPbwd2DwCDU4B7BuDOqezNTkcR12NyrVFiBlHSzrzDkDZSwOS8KdXo9y5RfyzAuOKMlpbEGW5Yl45G6bsipm2jiybPtalzHWsFoBeAflLY+Xk2f46HOderzFt7PNhxJYExh3FAsY2eGelF7AbMDtK2hGAeaS6IYToaF/Md2bzzOWOheyscBaCf1EDPrTAzO3K8fhJad3hP80JgXOhacrcOtZzKrHOrwxx2LPDfvPdWOApALxyLFBqFKSgcBaAXjsJROApALxyFowD0wlE4CkcB6IWjcBSOAtALR+EoHAWgF47CUTgKQC8chaNwFIBeOApH4Tj2QE/HNQlqjsW40gekjRDX6kro2gIjkTPm+31ygc8lj/C5RF51FpXrt3HBNWh50V/P95Hta5b7O/6fSnOY4g6es/9x7ScOaU8qZpO/I+VeP8vryH6HJJTokhbKufCZIZmgXGY6mZIyVFCSiOXM54lwSGQe3wqt23gqaZb44lx3Xj8pWUchLlujGb3g8u89jSMnIZ8gQOfY6kRKQRQJaBqXT0pJzzIkEvMPJT07sr9PLvD7I31uzu85ocIcaU5ojhvlhaJcZpEeXFrVXjBAzys2oSlSXios3Utm7ycA7kVGi44zObnqjPQq14850DWza2kkpeXNoWTMqLoAfYLLTXOp+VjixGo4yHIuoUotvWmahQjNs0eLSu13mQNaY5xKG+L7T6azuQHG/Z9EQGdJH9s7gOTv7kPsd/cidvPdNO5A7A93zj9uuWN2LOb3z+Jz0T/elR0zv78Lkaf3AGFVUiMZJCm8cDR6XvIGjfCv7gT+fC+if7g9O/Czu6D/5DbJINOTRkUVTlY51kBXSHhEHt0G/OY+Ou+ds+NmY4R+S9cWVEjpKazvTiyNbibbsAAN7x9B9Od3QfvN7bSe7pR1FKHX9C33IfHre6FPR6QqTwbsJxXQubTB8I9+jVEuM1zRC1tlNyarrVLO6NgOo9WtdOdYxPvDxd1wWDoxVNqKrTVrocQjohmf78yorEZPq9KOmeu+cNnnidIeDNfm34OnshO2kg7sufRLRhkoTQpAH7PryIw4mTj7rviK1HXLOz/NH9ehm6joRHj0IJllxIqSqROm4YGwGU6NZeKnKxi/+VZ4SjoxdrrRlTYzDwFu8VRqhWrz5Wn0E7mV8j8APUzSzP6Dn8O7tBleLipoaSIw1sPJpYeO6ZgF+mLeL10+uBVRZZNUDh17y3/Sw4y/YIDO9h43ImQ6rKeTGOdWTnUteffgpXu1FTdj7yc+d1yBHoUBdK8lfw65/pyDFvpEZQciY/0ECqPM7YkE9JRZ4CNF5qftt3/FdFE7xs5oM5pGmPMwXdaEKUs7knbPyQt0zn32fO9GOIob4Sxrh136bzflFQI8FiNT7VTa7yzi/ZPVdC0lLSShSUu9pgPjpd0IPfjICwboCXHs8KLh35E2sXRgeHlj3j14Lc2wFTVg78c+c1yBzgXa9v7HVzBRnT+HLm7aWMktndoQHR9AKq2fcECXApPsEqH/Jm7+K4LLWgjoLXnNJLgL7aSlBUmH8+QFOgt59w2/xTC3DK6Yrc3tMdvVcvF97rSR+Tmv/U6mhY+lRQobclVT7sjpIQnqLG8iM6BFeocFSs02PuaY+1nulOkwu4ZmqqROmE0HQ8tosXI3UQL+1MoL4KcHE9OiiKRSOQURzNxqM4c7bf5uMVVbn83I1+jGefh8KRKXo9w2aXlD3r35SFA5S9ux6xNXQ+d+6TmLbHbkpqXPkz+e1xBiIaCncOCKa0lAt2XnUOaRGJG8llmBQ8NctIZrP8kOQKad0/GYo9lrnB1HK8QWdU49Jb6H8d/eKuxleHl+m6gAzYmdNHpiaipvPnl3h2vbpeaUks7rwvssruNoawQcj7k/LNBzywIHig3wcuH9mRIDhI7y+YGeqV6aEQSZpvf2yhYpWOgpXxjoGbDzq63cKoO7lPhKjTLFDpP2s2QerWoHoiS7U1Hp5JELhlROMYVMqebnDugJjFqsRN2bjwLoR1g8iwA675TsJ6AzXeXuKC6zFZLRDqkdg5VWpPoHkeRr1ZGtbDPXMfhcLcKc1ZcdR/u9aQaprgnQx276i6yX8TnPYTFAX2jOn821qDm9APLKezwPczwv0F033CRAz3QKEc2ebZrXLKD3lJANTyOjLUSLM0hNoDrofewMmjE7btrLuTa5UQ98qM54n7ekxXAYWZqzg/tzMWNgYTFFFMtT2kgLtCmvLjmXI7bTuW10jSGHHYoek+2k2X1kc8GbU8sTbjTlSx/1yK3Iks6pCJPt6pIHdI2ATjZ6bX6zQm8O0LmlUIY2annfr8rQecM9c/707EjBYCfpjIpEpgDN7ANOphno3yBh2iYlm6fKmzFeQ/NaRAK4rAt7z7kQmLKR4k8joqmGGWE2adTM5ozZOvbIqOGjmDeugptKScFIuUcBMN2znlpgZ8x4WmxkZ8pp8b0s5lyZ/+Ta0yqBS8HITX8WRmmraZgH6G1ITE7OC/RM9dpMQcvcCjwLrw9jpJCJ/TCfrwzew+eS1vzkkjIf0v02Pfs5fZFzmjZH7nqcuzYz4/ABMzSvtht+g7EqQ4syyA0tmgF0Mw4s78WD1d14hjTtoap12TFU1Y3h8tUYKO/F8BmrMXVaI6ZLuXtmO4aJaoeXmZqaNL2NvmewvAs7K6zYQYsvM0ZrzkNf9VoCybnwl3TC/soV2FtZL91MsyBn4VBFdnplGxT3DM1fQqqQZhalngEBB02oihRajCsaNx09qsFbjlFz8K5ENM7FEZn1zu7D5gI9nSbaaKG5qGnJa4rgKW4iAWbF7ks/JwEbKbPhAi8sux6FU43I92ZG5vy5v+Obkf1v/jGzLZTOl+TcPmrHp79B52rHKAlNR3UHZk6th3P5OmxZcQG0cBhqIo5owpg3jknILmQOa0iZjWBNKZI4ynnjz2nSh85Yp0jookiSwPx+FX5kScNrETXvlcd8czJ35O2MyW2lMX7Hgxhd1oTx0ob8VlekOCbIDIyNj+e3stLN56lqCHGRTno+Ks9RTqfMw62ReA4nYbMoohDbpGcbIsEjAppbdvEF6kZoBbOpeM5nFzOfmXvUMufimoIpVVgDBwYtVKNv0UBnrzdr5smKLuDgFBKeEBCMIRGNZocSmYYaCEL3TmPyM9+Cu7oX/qo2ofhjVUz5G+R7HLQADxS1YebP9wB+er8/kh3pQARqlL7XH8DuT3wOEyXdiC/tlGvJtg4+AtCN4CjjwYW0JJJqElGVtH4qcdRD0+JQ6TuUZASBdIy0odE19VgAnSSH1HpX1BnZpuORTqvZcxv10o0R0eP0mqBFSHOUUs02yQsDfaR4FWx1XThIzGjiE9ciqivilZeGkPx+Y90hlIjR31QJKtGl72vC0EJ0L9rRzhs3ZkhzzIOCMC1lDmDhppUsSeYDOrMKLZ4QtpNQYgS4JOLcay2VyI6FzpVWjaFqCeFvOj2v0Z/dAieZKfa6tkUBXViMCXRwB5loBEbLjNmGXPOfn+5RMwakyKbxrIIRP1Lcpy+kZiM86SFLLzlmbIlULHvdcu1HnFOj7xwPKclL86TR53S6XkVTzQCsnLFYoDN1t5ldPGyVTfRv0syVvVDDUfjovUFTcmWGpqekDHCAtd2WPegj6miraTZsdGYD5atIYzeKg+TAug8hrEVFvOfZFQpNdiItr3C5sKv1nThU0YFg0Wx3EQE60fYs0Lm1sdk62KDuhkQX2ueLIHLtH/DUq3qw96Urj2786wrs/Nc3YMe/vB5bXvpG7FhzCRL3Pk4PRxUaxva2thiglzDQO7CHqHtKgG4ICvef7seWZd3Y/vJV2P1vK7Mjc/7ddP7M2PaSRux8zdsQ/smfARKqSVMb51I4dq7tuvJaw3lJJtPBinZEbruVtALNB8tnnwdKIIAkLbpQ0ux3Rtez6493YdNpHXjmJQ3Y/LIGPPWyVXiarmPPUc7bnn9bhWdeugoPv/wcjL/zv6A/sYuekyJATGcKYOYcUV7AdB2R3QPov+RzuPOl5+DgS9pw4F9WZsdC53rmFSux7eUrsetl9dj0kjfitlfQZ9/wFriX0rmXryKq3pzdXvMRnZ+w5AM9ZSoGDqCJTTnQ96Ev4W8vOQeH/rUFT/7bCjz5shXYRGOh82eez5aXnYNnXr5C5mzPS1bij7R24SZxwQKO7s3/t83YdeZb6H1N2P5SY24z44jzyfdJ381j4yua8Oi/rsKmszZg6Id/gOrwGKaG2eQzrT8LoGfa9jKwPOUdtFibMEwXnuIa4CZ1yAufZXrCvcbYBiMA7lzWQTa5aceXtUvDQCc3EiQ7feK8T0qzQF6oCzqVSMPs3fAhstWb8nuIyd57GyYJ7HG3V/at+YLSmaaG9J2qlhSttOuS/yKhsB5Dxc3z9hJ7NiPTD01MEbqXkZtuRTgZyVKpIwHdSbayh4C+76NXyQdYIIa27MVOEny+og5MF81/jc6c9kkBMnXGyNYepu9/ZMP7ocbpWaia+AUyQi5N2mLw0i8gZOnBgTe9FYrdjgg/rHga3oF+bCtugXd0xNhv5gtJsPswhclv/pwEUTfGSEC76JWDa1z03I92vqR/G93vRAWbbh0YeWkj3L/6swh4Dk1FClkBJXSTBM/wD36PbcsaMFlKtjWbHWWtizwfrU/uOlvagSlLF/Z0vgv+62+UQBlbbUvee0N0PTZ6jrGJCUM5wOh6m+Q9eKLqj75uDTHXHrjOXEPrtZkEg/HsnYu5jgqOVaB1f2oT9JIN8PzqFqMLb5jA/thWDNR2y7nZZ8XM9qjnVvwvVglmU6rPw/YVbyXmGhezKyZBQ8cR6Lq52IWiHAOgsxuk78KP0cS1Piugx/n8tIiVHTuJQdBkLKmXPeV/ZsHyg+YH7qf7YCcb7yo8c+Z6pJ/agRmipun0kTU6e8E5Om3fR64m9ZUUejpI8+CpW40pWiDums4jAt1WXo/ROv7ZCk/1avi/93sCjdFW2HDIsJ2r4ZlPXgfbf14PTAcQJxqrhyOY+PZPMUSCYpTMnvihIaNhBD3LWaD/TEyLsTJ+Zl3/NNBlEItx0vdN1tDzp+/eRSNyz/1E5RViQrrs5QsL4cXp9GLb8l7YXrECAQL6VFUTrZnGRZ3HYzF6yo3UtqGPu8/efS8mf34LfHQfXp7bRQBdIZCHHnwKvhJ6D7HXCRLMo2xqViwS5CLYDOfzoeVduKv5fKTCPigkYOEN4O7ei8hsaJedpswW8tGvyVa4S434gNEaNmV7se/Sa5AkE0yTzKV/Aui8Hz5YxUAPm0CfP1BFfpsDdIO6G0B38ZYbAXdqw2WyBZI6zDYRZ6vtf+vHhPYfEegxo+w5U3YlmULY60d/05vpPs6ma2+iybFK8E9mTFXNPyZJgmcGe6mnSxjUbXle/yn6G9/HeHUnDqx+h9GIREvleDoVAksnhuvajQjArDbooAXcjW2XfRE+NYjRK7+NA2RDjpLgYOExXN0s25eZ3uG+Eg7uaJfFk7UvS+pp8dL5ORZhOT2jkm4kZ3ziOc84YVQyfSJhhbR4hM4Tgvrn+7Cvbo0A3FnVSQu4E4mREeNBccJSXBMWNnndT0UgT4jjdRbofO0OmusxEtCZ6zvckDXDz5j9OxXGDgtvydprSYtVtZPGbSOgJxGThClNvEzsdzj4qS/DX9eJ8KtXyZoZqWn5hwhJtxmjwVGGuc9tgsA1urwHvmIrDr3vakxpJOB+9BeaM9Lo1R3mMzC+I8A7OgT0uGyvpUyPO/di1+D66g0Yr2qk+2iVXRJvWZv0p7eJouuQnZ5JbohJc8HXx2OU7nmS3j9FwiywtIm+uwm7T2lByuMmRUYmWkLFvg9+ntgFnbfUWDuTVca8TFW15YzZ+3GY3XUd0kq7NTuMKNHWrPBhoIeK6om9NWMfgV2ftMsGzRyF/uyBPpAFuv5PAv1y6Sd2OKCzQ2r/RR+Xjp6L0ehGRGdKNOroNTfAtpQobnU9XX+TLODclsRTPOnzjNy2wLZKesi0MO2V7bMaVdgFC4AWDBDQhonmIaDO8XQqGC0loC+fQ82YElf1YMulnwUO7MNe3p7kgBaJ9zc6qHLYsRF63CpBQhNVbXmdTyX4SARfG/qrGuAvJtDu7c/3tmo6AYnm1e/B3o9fRXPQDU9tFy0ueh70XCfoWSpE3Y08Ds0AOr1O/vf8QOdurw6zi2rm+uYOH/0tMzJRaAz0SXPh8tark+ZynOZkYNkqqGSrs19HshBJ42nEirasfpcAJk6skcE8XpXZ0s1hNJXGmCB2mfvcxrh5JF37IL0GBvtla2/st380/EvVprA1v2OmzAC6IkDXDDvdBLrty98jAd4kuzy8/serWrM0m1lARms7zY6zmZFRAmOlDWQ+dEn4bUiLQY+SFNvehz6a9+m6FgSr20njG0FgrNmnTIFojNn74W1RT8Zc5DVi+rkyPrPcyNJp3somJTFU3QvfrQ8jTROrzMnsPHGAbrQNQ4I9n1u24sDSRsyUrybwdNKwiv3mZMCaI1JknXeEyFbODKbq7JD0lLTkePzbjAdOi2qM/jZy1mok3JFs8MvhgO6pYOnfjqF3XIGRNR9F+ozVCLDWJruSx0wpnb+kU0aQfvbRebyWfI+xWyIH6QETBfbRPPhOaUVs8+48oEfZ8xyJYc8Fl2GINOQU2bwOS5NoEAct3HGa/9jYiNHfDUcG+iRTeZozN/dpN69v7ggWd2QHC0NxmFqMsFunCXgvXbODGEw/zYEWjSKmqJIfrhKFT0fD2NFyASZObyON20nCZbZvfJ7HnL7DTdrbX9GV99z8yzrheclKDF75BYR4ZcXicPzhLzRfzXBUNz9roPMuDz/7wToDgN5Sg2U5zEQhJ2EjWNqZN2aKaU2Q8N755k+QJucdDPpmMge2rDoPMWJ4KWIbseJ2YZdThC9nBV97W86YvR+282eHVYadfmYmIYFsOUD30Rq31/LcdGHi+pvJdDXSlI8K6LxVI9SdjP8XCtDZrk04TaArxqYi23qBv2/B9K/vguc3d0D9CY0f34HoT29H8ue3Zof/t7fNOyI/vwORn92B8I23I3LnY7jvrF6gbDUBwAgAYk3ikMg81lyk0c/oAVxxI/rJ9HbqOUDPS2rhz5E5sP/dn4L3brIF79sI//1PIn7nptlxuzno5+k/PYC7u99LD7AbtjPJprR0yP1zaCtrdHdpI5wlJHg37spPaiFhF/zLA0TVafFXGrTVYzq1eIGMk2aNkUaXuBVakBqtcga659qf5QC90wQ6Z3+14FAtUeq/Pjh7fXOGcufjSN79BNnFf8GWN16EyKuaMPP6Xnr+s4LOYZowdjKFEirNWCpmdFplOz0yg77mtwmr4bWSYTHySgI3dGobHiima//8DXDcfBd8v74Djt/ckx2u2x5BetchuqcEonpCHLHeX/5V7GW3aQtnTCh3dZtoaYxMZIOpxJGpqpj68vUkyBuza196y1sMim0jtrDvXxqw59P/A/vdD8N/70ZM37sJARrx256AdvdmqLsGaC0mzBiCJELTXkzd/je4ScMHfncHfL+7DcHf3o4ADX71//bW7Ij/4rbsSPzsLmPceBe0nz8AlcbOS6/D5tOaMX7a6xEobhbWKfZ5uUHrXYQv209/L3EKiXTq6IDueoECPZkD9EzwCXtPE9yxlJ1kClNDspOUlOzRZoZCD2G+QSgBIqoM9paq/f0YeO16Q6qXGXRu1jHWgVEBuiJRZRk7WafZyQI9d3uNF/lSsqU+fBXiSVW6psY5VDKdyhl6dsSTJEB8PvQ3vwUOeqChEsOhl8lBsBNNtJPmx+P5QI8RiLZd/U1Mls9xQJoaYIJYGQPdCEhJivRXCOi+BYA+WrYCB8nOxZQn7/pyh0IsIqLEiDIyVT2IPSRMJsoa5HyZ82c0vbO4VZ4P0hmgpwXoB5suFoFkL8+fNxt9lpOEtE07ZIsqSM81EYsJPc2MpKYaEW00+xF5Gkl4fnUbAb1DBHSuM85Vw0KH7mdoQgR0Fuj0HZNf/g4Bu2HObkmbJMGw0PR895fSuTbNe/0cqELzltSNZ8f3xHvwutkWm5OcUnxdpNUV1VhfxrqcHblrL3d9pmm98kgR20on6L5iRttsx3d+ATvNq9diRJXaqoxgNjGXOA36pzfLY1VS2okLdAmZ1I2ccCPaKE22qhFllRvdFsWRI5z4/qa9fnqASYxe9jVZGO4SovJVXUcNdHauTC5rxt6PXW1UezEbKEbpB2Po2evjKLBoTMGMGsWhz31FHENM73l770hAZwfQrk//N9xzt+uOEuh2si37+T6dvrw5zB2ZyDVOc+Z533juuyVmgE2PjDY9WqCPV5AWO3M9gumExG5E5Rz5UWVGTQDDP3HMgW4xaPx4UT2BY5JMjqSAMNMOmst2hWkWY2ZocsaESibJJCLgx4gpLCbybb75jMqc6vIzR2UiMC07CaM1LWTqsbP2ZAM6V6FiaU7SViP7NBEJQ9neh/TGHUhu2gaVRmzzluyIPjU7IlueyQ5l8zOI7tomM89CgiOS3FdeR7Yle41b4C9pP2qg+zm6b1kr9n3kszTPZkz0AmmqujmRXEfPfv2PECriB9mY9brOBXpugk2KtM3By66lRd72rIDu/frP4CzlRJg2Abib7GAek3XNOLi8C7B7FkzlzI0wi9IXD154aV5SVMaRKSnKxEx4W1WXbVrViOOPBbG77SLxRvvJls173tX1BDKrgEkKS2jpbHbiPyRypI8MdHutsb+PYaLuUkjPjKokITHx5e/CMWfePCxciaG4iC7HPE4jmIsjGI+Q7BRkERImMwozCI0MQtn0NNwbH0Ps6WeyI3cdxmjtZUb8qW1I0Jr1PvU0EqEgpmHEzSNGpknpOnpGhu/Da8lklvK/O+H4yc2i6BInskbnHVGOhtPtdvx93XswUtyC0NJOCQKxV3QjRtczO7rmHfGibhw6rRGx/QOIccQfaRHHZ66Dk7PASIp6So8e6KytHATYPR89vkBXid4euPxaen7PD9BZTx98y6XZ6/xnge4moA+WWQnAqvhg9MNk/B0PoLMTkgcnUj0boPO1zKTiGPn019BH2tb9ahL2LyfaTWsjMxZah56ybnrW3ThQQ+vxKz+SOn9SVIPMo5ClV+JR2NHpNrccTyqgM8g5KWLf+y5DpKiLHqhVttZ4X9RR3ogxWsCZMV7dMjuqmrNjsGKlFNzwPvq0WdMxgcnPXid7oF7xuh490GUPnhb5ro8dX6AnCAz7rrgWDsvzB/QDb71UtqiOBdA9VfXYX2GVGP20WWdvbiLP8QQ67zj4LOxzeHZAVznsddyBidpezFSRsiltxNQZ7dlYANlCzFmHY7T+MsNlaUS4qAkzdN6BS76AJG+XSbZMGDOktDzsMyg3Comc8ECfrKQFa/dK4gWvF6aMKTWOvto1skc5XtmUF2xiI/t6aplVEhomqpowUt0qcfe81ZIZ41UEHna6PLCRFj8tWj0J+5Xfpu+jaycAuOmBHS3QfXlpqun/3961xcZxVuG+IdFL7HV8i9sqrUBqqMCxHd9qGtJSKFWTNlSCUmgRLy0tBbUNgpciQCoSSuEFJRUgBE0rgSgPfeSBInqHpmmaOk7juLG996t3fd3L7OzsHM53/pnZGXvX6ySmruj80tEm3t3Z/z//+f7rOd+xCDKqjYHOgwH801NP/5YybPzJlgFnr7t2j244gtDQMxcxo7v36HEGeKaTZxaWWV7JnL6WfyeebAh0d79h5j1958MU2bGnKdDRPgnGyC80BHq8q59muljPZrl5TLu5+UCXqyyuV7qVZ+BcrBai5oTLmXX1oBd49n3uRZoKfE4iNsEHgFcQf0xj6c1gDgf2yNVvkgcytx1GcZ7Dn03xKuJ9thetaoX9lUq0GNiruBbtFYcPdC/Qg1cPMLDHeI8zRrnAboqyokNw7AgMOJJu3U05XrqnX3nVB7oP9EsCOlYq0SPH+PdG5SAWNimEKz2s1yt2kx4YoyjbXAIkLS4bhExhJQonoCvZZh/8MS9Uyioc1wd6c6Av8qh5qv8Avf6Z2+nUnjvo+PB+emfwbjrZt78mN91D/xq8neJvn/SB7gP90oDO/RB/5nmabu9TZCwgvQgMUqSjjxYYCyd4uT7Rfzed6t1PEwMHPXb4xuBd9DrL8QF+/dlhceYRv4ePJ9BHGOhzKg5YB0MKWBKKdPbaW2UPE+zu9wD93NDX5DBDYtdNXYWxaqt42eGzbsmysLWUeY/+Czk4gQsnjN8HutmEhbZC793xkDD21gM6SD7LuFvGhZFlwGVthc71179eS/BzYjv2UXEDRJbQvm6UhM7r/LMvsM7h3z/sAUZDoBs6hZ48THEAcxOADmbg2DPHaC4wJD7zmU4V+xDkgSvdeQst/+4vbAdFEt7yinXuYCgbNDVd+AoqyFBk4BASzmC4S8zTfPc+cc+2PeN8oK8C+pnbHiDACw4euGtGxpeSaXhJ/IyaLOEuFJFoh56SGX0O3OhdPtA/bKDPdg/yUvbztFwtN+VJM1xA/+DYCzKjp7u8etgKoKc64BHIK5wdcGndQ6GrRmjlT39Tq1GrDs71KOi3nMQSSN9VErDL1WJxhRY69jph0yl/Rl8L9PHb7lcMcjp8kE2h+SmTvirLiunIIhIyGBrNMNDhQLLQ4QN9K4AeZZ0lLx8h4+xsQ5ZVWyRPnwvoqfZRcT3eaqCL+y3rHZFvCcZRtOUmmv/jXxm8ReG4s1mKKpJn0JBoQiGPEKAXWDQBO60sU4a3MeLW3GHJVt2jS7OTOQF6omfofwr0UjKDaASLWwzXawWa3HmbAD0k1xQ1oEeuv5VO3vcIvfSdQ/TaNw7Rq998jF751g9YHnMEf7Pl5Xu/T29+m197vyLBBMrPfOjjB/Rre+n0NXvXvV5rtke3I9rkinH7kOw5ha4KtFJwAS1k6fTgQdFzLjCiDBhx45ituvdSimV81y00sWs/nWGZ/dR+OnvDAUcmbzgocm7XQXr/hjvp3O4DNH7dzUI8ke1EAMnIlhzGxY8+L/yINm05WHkTbAfz7fvo7VvvoxP3Pu6I2w5r8ji9/MAheumBJ+gfbLfv3fcEzYCYtV25wAJL7hn9Q/WM+6gCPdR5Iy229omiQQCQ2z5IC20DwhRqy2KgJtkWECsOUg6hil19lvT7QN9EoGtSB94iacs0PvhV+dzKNi/QMz3D3FcDtMD9c3pHL4339NJkVy9NdXzWkfP8f1uCO9hOu/toGhFd6G+QQ7r8/rcC6G4qcxCcZrYNUviqAd6v18Rth45wuzMtAxI9B0/H7FWgwuplPQ1IUEtESFN9oHuAPts+IO2YD4xKBBfimtMdA8JOYos7+P9cz6iQVMyD0759WKLGPPfyPtAvGehLOn9Hqwqh4tuj93DdkKTDC/REzxiFeRbLtcFxhQda3pJlEGHGM7UjVjx/shsJPnp5oOYBgpfMIem7UQkG2kqgxy2QC5X51aM0wYNToqPP4zzjtkOPdKoYhzDj6Cw48C7/NGWFH0BFrl3UjI50v/HfHGNlMSC2WymTunlEbQcBwQB9ALK7ypLsh+sB3dnrpuboLbiLXqNcP1Vnqz17lv8+/aWHCNmrV4fTebOClmiCgS4NWWWwtXj0OVZ6xeI/Vvui4zu/IL8pHkZdIx5eMVsyuC6TuOex2l7HMgbEoS+0wXtumJYDVmhlt+pw9zUN4tJnrhvjti5KHm5sNqEV5P2absMg4KVhghHnrlQusJjKBGfmOumkcPbCn4r++ihleTkbBi2XEEGoNswF+mnpilEq/vuU11GDgT7x8M8V0YXr94WVBKSarBNzcsqhcsbNA1IYRX/5e8X0K1dBY9xuuA8zyHr20KmdI8IFvxGgF/mp79796Jp+i1knxQnWbanCLeNle0m83ISDjE796Cnef+6hSQYAMvqkrXh2m/QBnpAgpghePSSsPKibI501XjcQVkAQPw5dQdxL9xwGHLZvPRiuDbSgANM1Cv/kaf69/lVAHxSHlhjrZiUbVYQdleZZZYCRxJHnKLUNDMpq24dBGl6HwR517ee2vUbiHnBiluD/WYvLDhFs2Q6c5nNbjxyT+/ZyszDVJQZK8OgxCnd6gZ7pUMQTU92jZOqLEkBSqUPE7wA9maU3eLZJ7xh20jpleLCA0cyxkmc2AvSKThMHHpYRuR7QQcBQwIxeUUAXNtSKRidu/jqlWxhUIDoASQCYW6CwriFHFgKgkB7j99cCPWUddADoUCZemwFdk6ADKxKrUqIzrK/p6731RiBCZtsQvfXgD8kslWVG16tGU6BHGOjojxxvJyI9w5aB4FCnn4qf5Nl5FdDLrI/x7/5UtiiryS0xS4b4WfrkOTlzLAja1wIdAyEkzQLSiFNwgY1s7DAOtFAnGeirOdHqA12lkJLDo9kUndgxRpGdo7IsTXRZsdZWLgCANydsNkOWDsZcUutD8PlBMHsmLOILN+fbgpy1jJAWCiv3W4vrcENAz0RU5KHRHOiI8zfeepeCSFTSruinAPZc25hgQQJSLgDo9iQkZJUdNaCjf5YYq+dx2PfMMUXAYjYBOk5MzzPQJ9uGBCxhHongMhrlZROWjhM8upqFBRmtwA5SD+gSLhjN0T95uRmHgwA3FMEcidZhmuJVQYSf9cGXHyHQzsuVQaOZQTdo/MCjFGu5iaKS6rYm8Bmf5oYW4xkykeCelS/XL0h4/5/j9OaN++hsS7+wwISxXGplY2mrSQhsoTzrxngZH+clni3RNvVsafd2pYOZDqUDLDnt9yF4f3InTqNzVEL8cUXCpdlwS3ScR9dJXiJG2moSxDN5j3UCKZmKZcUU3gToSD8RPXyUZzleXVwxSNNdyuEEoZ4z2/tp4RMjVHjNG6ZaZNC8y0A/3zLg1BUSQxu5HjMgfjhzlgFpSmgsOJ1wjRg6/AcKc3vPg9CxBf3NM2HrKLd9mN7B0n02oQaydYAuBJ28HTh+1/coKHaj9A0bgE6hwzDbglZmoJfV1kS4zrkeqXyJMn/+O726ax8FO1W/JQLoKx7gwOLbwktgPG/7oLwX5j60RdyaLQny5yH4Hk74Y/L76rfxCi7AKf5ceWZW0RKZapIwGOizT/6KZgN9Hr3h9wDyUAvbWzSomGOqzYFeLZFsY8a/eD9lWnlVwvqPcNuTrdArr1BA7uiyvXoSs2zSFvffk4h/aIN98gDIE8gED6LnjzwLN3y5UVoX6Fms71nhlUSKjFSM9HSMtEyMylEeyUIRKiWiYhiStNCoP6OD8hkxw9nwDOmQZIjy/BwjGqZyLEx6lPc5s1mKIexQNxpmKE2zwRRn+femQlRMzjhSTkVF9GSc0mBA5T1etph3EjgsgfVUK3Kdo7SSnqViJkiVZJA0/o4tZZdc6N8d4XZV0nG5osNKCHfvZdBdY0GcypCRm6dyLusIZbJUSiapkF8U4y5LEqHGpYS7U0TkaStEuQwVFuJU4L7QUnF+DmsvGaVKKE5xT04vNlreFpSjcd5TJzz1LSbDIoUklqwlKsi9FslSX4JBeA+uR+Kkx4Lcz+izCFXYBpZY53nuuwV1Tl6L365D9402wffDSHF7w/y7Gd4Hp6GncE2fiYgAQPYNrsfk+ZnL4OhfKJKxlCZjLk5GPHLx/eN6H+0upSLyWp1LUD4eokUz7yRWkGs5nSu+wLqOxDzPKFl6W4nOIAUF5QzNSg/TJKst1IqBZD5PWi5FWjxKy/Hw5tgh48kWjZ9pREL8GmKbzFG8vEx5kH6um3sNPPNFbrhmSj9YW1/Zu+fFPAxaZFBpur6WatICOi76NQ2ZNXTJs1WU/KIq20Ololg3EJCPvF9gz2gE9GX+bpmXuDBClZFLiTB2WiKja8mgeYv7S1wg2dIQYgoyexySaWKAjZ9xoX+3RbgTcD2EJAgAi+WwUeKVBfKaSVKSak2WLDIBQ65HDVk2rgd0LL8w4y9D59y+oqEGUd3KSQaKaaG2znuBbkDPhil1cNfXTrSh40NgLsmXuU5VydgCwo6CWRE9gQ0Fna7ZaYDgqYV+040NAR1eXOhnlR0JWzxF62zrUtaBhYqkPHI/BauholmRVUxe+o0UA89F9s/qz+hWwhHe20g+NLNU9SatRKi7ZDmhVXpTddCsNNMF8a+oNgd6sSrbqEXJUMNtQnYWcdm6dDvUXf25QooMFP3qpJAqN6V7NiQ0smwlrEPWB0Ml/XayVarkcep19UmxjI6ufGCGHY5ZVYwqyntJPZdMc11DV/t9lXmikVStFESy4XRGK9OihDWcUFBxRljnORcjKh+6cpd1h03a/1ZJ8VyJ76rKGQKUR+4kjQ3bb9ZSPqvBslpLPujx6PNmHwVPu4mDScNbX90SSe7ncgzSrUSUGEDsWG/DWplJSKgkeFGUUcY6OcRtoNsJG1dQX8Ow6uzSv6lywVZW3bgYrvYYVr9WN6nfdKs98ip+9sohxetsYwg11Np+rsqh4RJSVVn1MtY7RHXM0Ob6t1YMpmElctxcMVyvRdy62ElF1wM6DKAso061YX7nRoncHKCb9T+vWZlAxcA2kCO7nudTozq5jc+wrq0qVHUygoo0ed6lyGbly643O7i99cyqGmylf8z6z5NrxqpMT/Xra9rg9iTzVVedFrhKFvjJmuGK1vhZ3QDQyXo+Vn/uurnr2qi9zextK4Rcg61t39UNJHnfijaojLjmGnhdVu8C13szWGdJ0qhhDYBuF91JPbsBlG+w1PsdV/LLhvnEN7tcaL7qiwW6o+dVfeTNy+36XqN+apA33ga6TvUPljcE9A2270L7dSuLUx+XbX0U26Dbg5DZDOiboZRLfN8vl6hj88Pry9Wf9fv2o2kXl/mq8Ytf/v+LD3S/+MUHul/84hcf6H7xi198oPvFL37xge4Xv/jFB7pf/OIXH+h+8YtfNlz+C+CT4iEdcTIyAAAAAElFTkSuQmCC">
          </div>
      <div>
        <div class="logo-text">Mahindra</div>
        <div class="logo-sub">Predictive Maintainence Dashboard</div>
      </div>
    </div>
        <div class="hdr-right">
            <div class="pill pill-g" id="machinePill">
                <div class="dot dot-g"></div>
                <span
                    id="machineLabel">SENSOR ONLINE</span>
            </div>
            <div class="pill pill-w">
                <div class="dot dot-w"></div>WATCH: Y-AXIS
            </div>
            <div class="clk" id="clk">--:--:--</div>
        </div>
    </div>
</header>

<main>

    <!-- KPI ROW -->
    <div class="sec">KEY PERFORMANCE INDICATORS</div>
    <div class="kpi-row">
        <div class="kpi"
            style="--ka:#0ea5e9;animation-delay:.04s">
            <div class="kpi-lbl">X — RMS Velocity</div>
            <div class="kpi-val" style="color:#0284c7"
                id="k-xv">—</div>
            <div class="kpi-unit">mm/s RMS</div>
            <div class="kpi-d st" id="k-xvd">loading…</div>
        </div>
        <div class="kpi"
            style="--ka:#6366f1;animation-delay:.08s">
            <div class="kpi-lbl">Y — RMS Velocity</div>
            <div class="kpi-val" style="color:#4f46e5"
                id="k-yv">—</div>
            <div class="kpi-unit">mm/s RMS</div>
            <div class="kpi-d st" id="k-yvd">loading…</div>
        </div>
        <div class="kpi"
            style="--ka:#10b981;animation-delay:.12s">
            <div class="kpi-lbl">Z — RMS Velocity</div>
            <div class="kpi-val" style="color:#059669"
                id="k-zv">—</div>
            <div class="kpi-unit">mm/s RMS</div>
            <div class="kpi-d st" id="k-zvd">loading…</div>
        </div>
        <div class="kpi"
            style="--ka:#f59e0b;animation-delay:.16s">
            <div class="kpi-lbl">Peak Acceleration</div>
            <div class="kpi-val" style="color:#d97706"
                id="k-pk">—</div>
            <div class="kpi-unit">m/s² PEAK</div>
            <div class="kpi-d st" id="k-pkd">X / Y / Z</div>
        </div>
        <div class="kpi"
            style="--ka:#ec4899;animation-delay:.20s">
            <div class="kpi-lbl">Temperature</div>
            <div class="kpi-val" style="color:#db2777"
                id="k-tmp">—</div>
            <div class="kpi-unit">°C INTERNAL</div>
            <div class="kpi-d st">WARN: 85°C | CRIT: 100°C
            </div>
        </div>
        <div class="kpi"
            style="--ka:#10b981;animation-delay:.24s">
            <div class="kpi-lbl">Machine Status</div>
            <div class="kpi-val"
                style="color:#059669;font-size:15px;padding-top:5px"
                id="k-ms">RUNNING</div>
            <div class="kpi-unit" id="k-noise">Noise: — dB
            </div>
            <div class="kpi-d dn" id="k-reboot">● Reboot
                count: —</div>
        </div>
    </div>

    <!-- WAVEFORM + SPECTRUM + PREDICTION -->
    <div class="sec">REAL-TIME WAVEFORM & SPECTRUM</div>
    <div class="g-main">

        <!-- Waveform (Plotly) -->
        <div class="card">
            <div class="card-t">Velocity Waveform <span
                    class="badge b-live">LIVE</span></div>
            <div class="card-s">Time-domain RMS velocity ·
                rolling 60-point window · selected axis
            </div>
            <div class="atabs" id="wtabs">
                <button class="atab ax"
                    onclick="setWAxis('x',this)">X-AXIS</button>
                <button class="atab"
                    onclick="setWAxis('y',this)">Y-AXIS</button>
                <button class="atab"
                    onclick="setWAxis('z',this)">Z-AXIS</button>
            </div>
            <div id="waveChart" style="height:160px;"></div>
        </div>

        <!-- Spectrum (Plotly bar) -->
        <div class="card">
            <div class="card-t">Frequency Spectrum — 10
                Harmonics <span
                    class="badge b-ok">FFT</span></div>
            <div class="card-s">RMS acceleration amplitude
                per harmonic · read from
                Vibit_[x/y/z]_rms_acl_amp_Nx</div>
            <div class="atabs" id="stabs">
                <button class="atab ax"
                    onclick="setSAxis('x',this)">X-AXIS</button>
                <button class="atab"
                    onclick="setSAxis('y',this)">Y-AXIS</button>
                <button class="atab"
                    onclick="setSAxis('z',this)">Z-AXIS</button>
            </div>
            <div id="specChart" style="height:160px;"></div>
        </div>

        <!-- AI Prediction -->
        <div class="pred-card">
            <div class="card-t">AI Fault Prediction <span
                    class="badge b-ml">ML MODEL</span></div>
            <div class="card-s">Hover each fault for full
                calculation breakdown</div>
            <div class="rul-box">
                <div class="rul-val" id="rulV">847</div>
                <div class="rul-lbl">HOURS REMAINING USEFUL
                    LIFE</div>
                <div class="rul-sub" id="rulSub">≈ 35.3 days
                    · Confidence: HIGH</div>
            </div>
            <div class="fault-list" id="faultL"></div>
            <div class="pred-info" id="pCD">Next ML update
                in 5s</div>
        </div>

    </div>

    <!-- HEALTH + TEMP + EVENTS -->
    <div class="sec">DIAGNOSTICS & CONNECTIVITY</div>
    <div class="g-bot">

        <!-- Health ring + gauges -->
        <div class="card">
            <div class="card-t">Machine Health Score <span
                    class="badge b-warn">WATCH</span></div>
            <div class="card-s">Overall vibration severity ·
                ISO 10816 · computed from RMS velocity</div>
            <div class="ring-wrap">
                <div class="ring-rel">
                    <canvas id="ringC" width="130"
                        height="130"></canvas>
                    <div class="ring-inner">
                        <div class="ring-score" id="hScore">
                            —</div>
                        <div class="ring-txt">HEALTH %</div>
                    </div>
                </div>
                <div class="gauge-row">
                    <div class="g-item">
                        <div class="g-val"
                            style="color:#0284c7" id="gX">—
                        </div>
                        <div class="g-track">
                            <div class="g-fill" id="gXf"
                                style="width:0%;background:#0ea5e9">
                            </div>
                        </div>
                        <div class="g-lbl">X mm/s</div>
                    </div>
                    <div class="g-item">
                        <div class="g-val"
                            style="color:#4f46e5" id="gY">—
                        </div>
                        <div class="g-track">
                            <div class="g-fill" id="gYf"
                                style="width:0%;background:#6366f1">
                            </div>
                        </div>
                        <div class="g-lbl">Y mm/s</div>
                    </div>
                    <div class="g-item">
                        <div class="g-val"
                            style="color:#059669" id="gZ">—
                        </div>
                        <div class="g-track">
                            <div class="g-fill" id="gZf"
                                style="width:0%;background:#10b981">
                            </div>
                        </div>
                        <div class="g-lbl">Z mm/s</div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Temp & Noise -->
        <div class="card">
            <div class="card-t">Temperature & Noise Level
            </div>
            <div class="card-s">Vibit_temp_c & Vibit_Noise ·
                live values</div>
            <div
                style="display:flex;align-items:baseline;gap:6px;margin:6px 0 2px">
                <div class="temp-big" id="tmpV">—</div>
                <div
                    style="font-size:18px;color:var(--muted)">
                    °C</div>
            </div>
            <div
                style="font-size:9px;color:var(--muted2);font-family:'Space Mono',monospace;margin-bottom:14px">
                WARN: 85°C &nbsp;|&nbsp; CRITICAL: 100°C
            </div>
            <div
                style="font-size:10px;font-weight:700;margin-bottom:6px;color:var(--text2)">
                ACOUSTIC NOISE</div>
            <div style="font-size:26px;font-weight:700;color:#059669;margin-bottom:6px"
                id="noiseV">— dB</div>
            <div class="noise-bar">
                <div class="noise-pin" id="noisePin"
                    style="left:0%"></div>
            </div>
            <div
                style="display:flex;justify-content:space-between;font-size:8px;color:var(--muted);font-family:'Space Mono',monospace">
                <span>0 dB</span><span>50 dB</span><span>100
                    dB</span>
            </div>
            <div
                style="font-size:10px;font-weight:700;margin-top:14px;margin-bottom:5px;color:var(--text2)">
                TEMP TREND</div>
            <div class="spark-row" id="sparkR"></div>
        </div>

        <!-- Connectivity & Events -->
        <div class="card">
            <div class="card-t">System Events & Connectivity
            </div>
            <div class="card-s">Live connection status from
                result data</div>
            <div class="conn-list" id="connList">
                <div class="conn-item"><span
                        class="conn-name">MQTT
                        BROKER</span><span
                        class="badge b-ok"
                        id="mqttBadge">CONNECTED</span>
                </div>
                <div class="conn-item"><span
                        class="conn-name">NETWORK</span><span
                        class="badge b-ok"
                        id="netBadge">CONNECTED</span></div>
                <div class="conn-item"><span
                        class="conn-name">LED
                        STATUS</span><span
                        class="badge b-ok"
                        id="ledBadge">OK</span></div>
                <div class="conn-item"><span
                        class="conn-name">REBOOT
                        COUNT</span><span
                        style="font-family:'Space Mono',monospace;font-size:12px;color:#d97706;font-weight:700"
                        id="rebootBadge">—</span></div>
            </div>
            <div
                style="font-size:10px;font-weight:700;margin-bottom:6px;color:var(--text2)">
                RECENT EVENTS</div>
            <div class="ev-log" id="evLog"></div>
        </div>

    </div>

    <!-- 24H TREND (Plotly) -->
    <div class="sec">24-HOUR RMS VELOCITY TREND</div>
    <div class="card" style="margin-bottom:24px;">
        <div class="card-t">
            RMS Velocity — All Axes (Vibit_x/y/z_rms_vel)
            <div
                style="display:flex;gap:14px;font-size:10px;font-family:'Space Mono',monospace;">
                <span style="color:#0284c7">— X</span>
                <span style="color:#4f46e5">— Y</span>
                <span style="color:#059669">— Z</span>
            </div>
        </div>
        <div class="card-s">Historical RMS velocity from
            result data · hover for exact values</div>
        <div id="trendChart" style="height:220px;"></div>
    </div>

    <!-- HARMONIC DETAIL (Plotly) -->
    <div class="sec">HARMONIC AMPLITUDE & FREQUENCY DETAIL
    </div>
    <div
        style="display:grid;grid-template-columns:1fr 1fr;gap:14px;margin-bottom:24px;">
        <div class="card">
            <div class="card-t">RMS Acl Amplitude —
                Harmonics 1X–10X</div>
            <div class="card-s">Vibit_[x/y/z]_rms_acl_amp_Nx
                · latest snapshot · all axes</div>
            <div id="harmAclChart" style="height:200px;">
            </div>
        </div>
        <div class="card">
            <div class="card-t">RMS Vel Amplitude —
                Harmonics 1X–10X</div>
            <div class="card-s">Vibit_[x/y/z]_rms_vel_amp_Nx
                · latest snapshot · all axes</div>
            <div id="harmVelChart" style="height:200px;">
            </div>
        </div>
    </div>

</main>

<footer>
    <span>VIBIT Predictive Vibration Intelligence
        v2.4.1</span>
    <span id="lastSync">Last sync: —</span>
    <span>Powered by result[] · DEVICE: VBT-A12-004</span>
</footer>

<!-- Rich Fault Tooltip -->
<div class="ftip" id="faultTip">
    <div class="ft-head">
        <div class="ft-htitle" id="ft-title">—</div>
        <div class="ft-hsub" id="ft-sub">—</div>
    </div>
    <div class="ft-body">
        <div class="ft-sec">
            <div class="ft-sec-t">Detection Algorithm</div>
            <div class="ft-formula" id="ft-formula">—</div>
        </div>
        <div class="ft-sec">
            <div class="ft-sec-t">Feature Contributions
            </div>
            <div id="ft-features"></div>
        </div>
        <div class="ft-sec">
            <div class="ft-sec-t">Per-Axis Confidence</div>
            <div id="ft-confidence"></div>
        </div>
    </div>
    <div class="ft-foot" id="ft-foot">—</div>
</div>

<div class="stip" id="stip"></div>
