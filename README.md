#container {
    --bg: #f0f4f8;
    --surface: #fff;
    --surface2: #f8fafc;
    --surface3: #f1f5f9;
    --border: #e2e8f0;
    --border2: #cbd5e1;
    --accent: #0ea5e9;
    --accent2: #6366f1;
    --accent3: #10b981;
    --warn: #f59e0b;
    --danger: #ef4444;
    --text: #0f172a;
    --text2: #334155;
    --muted: #94a3b8;
    --muted2: #64748b;
    --sh: 0 1px 3px rgba(15, 23, 42, .08), 0 1px 2px rgba(15, 23, 42, .05);
    --sh-md: 0 4px 16px rgba(15, 23, 42, .10), 0 2px 6px rgba(15, 23, 42, .06);
    --sh-lg: 0 12px 32px rgba(15, 23, 42, .14), 0 4px 12px rgba(15, 23, 42, .08);
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

#container {
    font-family: 'DM Sans', sans-serif;
    background: var(--bg);
    color: var(--text);
    min-height: 100vh;
    overflow-x: hidden;
}

#container::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image: radial-gradient(circle, #94a3b8 1px, transparent 1px);
    background-size: 28px 28px;
    opacity: 0.18;
    pointer-events: none;
    z-index: 0;
}

/* HEADER */
header {
    background: var(--surface);
    border-bottom: 1px solid var(--border);
    position: sticky;
    top: 0;
    z-index: 200;
    box-shadow: var(--sh);
}

.header-inner {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 12px 28px;
    max-width: 1680px;
    margin: 0 auto;
}

.logo {
    display: flex;
    align-items: center;
    gap: 12px;
}

.logo-icon {
    /*width: 38px;*/
    /*height: 38px;*/
    /*background: linear-gradient(135deg, #0ea5e9, #6366f1);*/
    /*border-radius: 10px;*/
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 19px;
    /*box-shadow: 0 4px 12px rgba(14, 165, 233, .28);*/
}

.logo-text {
    font-size: 20px;
    font-weight: 700;
    letter-spacing: 3px;
}

.logo-sub {
    font-size: 9px;
    color: var(--muted);
    letter-spacing: 2px;
    font-family: 'Space Mono', monospace;
}

.hdr-right {
    display: flex;
    align-items: center;
    gap: 14px;
}

.pill {
    display: flex;
    align-items: center;
    gap: 7px;
    padding: 5px 12px;
    border-radius: 20px;
    border: 1.5px solid;
    font-size: 10px;
    font-family: 'Space Mono', monospace;
    font-weight: 700;
    letter-spacing: 1px;
}

.pill-g {
    border-color: #10b981;
    color: #059669;
    background: #f0fdf4;
}

.pill-w {
    border-color: #f59e0b;
    color: #d97706;
    background: #fffbeb;
}

.dot {
    width: 7px;
    height: 7px;
    border-radius: 50%;
    animation: blink 2s infinite;
}

.dot-g {
    background: #10b981;
}

.dot-w {
    background: #f59e0b;
}

@keyframes blink {

    0%,
    100% {
        opacity: 1;
    }

    50% {
        opacity: .3;
    }
}

.clk {
    font-family: 'Space Mono', monospace;
    font-size: 10px;
    color: var(--muted2);
    background: var(--surface3);
    padding: 5px 10px;
    border-radius: 6px;
    border: 1px solid var(--border);
}

/* LAYOUT */
main {
    position: relative;
    z-index: 1;
    max-width: 1680px;
    margin: 0 auto;
    padding: 20px 28px;
}

.sec {
    font-size: 9px;
    letter-spacing: 3px;
    color: var(--muted);
    text-transform: uppercase;
    font-family: 'Space Mono', monospace;
    margin-bottom: 12px;
    display: flex;
    align-items: center;
    gap: 10px;
}

.sec::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--border);
}

@keyframes fadeUp {
    from {
        opacity: 0;
        transform: translateY(12px);
    }

    to {
        opacity: 1;
        transform: translateY(0);
    }
}

/* KPI */
.kpi-row {
    display: grid;
    grid-template-columns: repeat(6, 1fr);
    gap: 12px;
    margin-bottom: 20px;
}

.kpi {
    background: var(--surface);
    border: 1.5px solid var(--border);
    border-radius: 14px;
    padding: 14px 16px;
    position: relative;
    overflow: hidden;
    box-shadow: var(--sh);
    transition: all .25s;
    animation: fadeUp .45s ease both;
}

.kpi:hover {
    transform: translateY(-2px);
    box-shadow: var(--sh-md);
}

.kpi::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 3px;
    background: var(--ka, var(--accent));
    border-radius: 14px 14px 0 0;
}

.kpi-lbl {
    font-size: 9px;
    color: var(--muted2);
    letter-spacing: 1.5px;
    text-transform: uppercase;
    margin-bottom: 6px;
    font-family: 'Space Mono', monospace;
}

.kpi-val {
    font-size: 26px;
    font-weight: 700;
    line-height: 1;
}

.kpi-unit {
    font-size: 9px;
    color: var(--muted);
    font-family: 'Space Mono', monospace;
    margin-top: 3px;
}

.kpi-d {
    font-size: 9px;
    font-family: 'Space Mono', monospace;
    margin-top: 6px;
}

.up {
    color: var(--danger);
}

.dn {
    color: var(--accent3);
}

.st {
    color: var(--muted);
}

/* GRIDS */
.g-main {
    display: grid;
    grid-template-columns: 1fr 1fr 370px;
    gap: 14px;
    margin-bottom: 14px;
}

.g-bot {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 14px;
    margin-bottom: 14px;
}

/* CARD */
.card {
    background: var(--surface);
    border: 1.5px solid var(--border);
    border-radius: 16px;
    padding: 18px;
    box-shadow: var(--sh);
    animation: fadeUp .5s ease both;
    position: relative;
    overflow: visible;
}

.card-t {
    font-size: 12px;
    font-weight: 700;
    letter-spacing: .5px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 2px;
}

.card-s {
    font-size: 9px;
    color: var(--muted);
    font-family: 'Space Mono', monospace;
    margin-bottom: 12px;
}

.badge {
    font-size: 9px;
    padding: 2px 8px;
    border-radius: 5px;
    font-family: 'Space Mono', monospace;
    letter-spacing: 1px;
    font-weight: 700;
    border: 1.5px solid;
}

.b-ok {
    background: #f0fdf4;
    color: #059669;
    border-color: #10b981;
}

.b-warn {
    background: #fffbeb;
    color: #d97706;
    border-color: #f59e0b;
}

.b-live {
    background: #fef2f2;
    color: #dc2626;
    border-color: #ef4444;
}

.b-ml {
    background: #eef2ff;
    color: #4f46e5;
    border-color: #6366f1;
}

/* AXIS TABS */
.atabs {
    display: flex;
    gap: 5px;
    margin-bottom: 10px;
}

.atab {
    padding: 3px 11px;
    border-radius: 6px;
    font-size: 10px;
    font-weight: 700;
    cursor: pointer;
    border: 1.5px solid var(--border);
    color: var(--muted2);
    font-family: 'Space Mono', monospace;
    background: var(--surface3);
    transition: all .2s;
}

.ax {
    background: #e0f2fe;
    border-color: #0ea5e9;
    color: #0284c7;
}

.ay {
    background: #eef2ff;
    border-color: #6366f1;
    color: #4f46e5;
}

.az {
    background: #d1fae5;
    border-color: #10b981;
    color: #059669;
}

/* PLOTLY overrides – remove default bg */
.plotly-chart {
    width: 100%;
    border-radius: 8px;
    overflow: hidden;
}

/* PREDICTION */
.pred-card {
    background: linear-gradient(160deg, #fff 0%, #f5f3ff 100%);
    border: 1.5px solid #e9d5ff;
    border-radius: 16px;
    padding: 18px;
    box-shadow: var(--sh-md);
    animation: fadeUp .5s ease both;
    position: relative;
    overflow: visible;
}

.rul-box {
    text-align: center;
    padding: 12px;
    background: #fffbeb;
    border-radius: 12px;
    border: 1.5px solid #fde68a;
    margin-bottom: 12px;
}

.rul-val {
    font-size: 32px;
    font-weight: 700;
    color: #b45309;
    line-height: 1;
}

.rul-lbl {
    font-size: 8px;
    color: var(--muted2);
    font-family: 'Space Mono', monospace;
    letter-spacing: 2px;
    margin-top: 3px;
}

.rul-sub {
    font-size: 9px;
    color: var(--muted);
    font-family: 'Space Mono', monospace;
    margin-top: 3px;
}

.fault-list {
    display: flex;
    flex-direction: column;
    gap: 7px;
}

.fault-item {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 9px 11px;
    border-radius: 9px;
    border: 1.5px solid var(--border);
    background: var(--surface);
    cursor: pointer;
    transition: all .22s;
    position: relative;
}

.fault-item:hover {
    border-color: #a5b4fc;
    background: #f5f3ff;
    box-shadow: 0 2px 8px rgba(99, 102, 241, .12);
}

.fault-name {
    font-size: 11px;
    font-weight: 700;
}

.fault-sub {
    font-size: 8px;
    color: var(--muted);
    font-family: 'Space Mono', monospace;
    margin-top: 1px;
}

.prob-wrap {
    display: flex;
    align-items: center;
    gap: 7px;
}

.prob-track {
    width: 58px;
    height: 5px;
    background: var(--border);
    border-radius: 3px;
    overflow: hidden;
}

.prob-fill {
    height: 100%;
    border-radius: 3px;
    transition: width 1s ease;
}

.prob-pct {
    font-size: 11px;
    font-family: 'Space Mono', monospace;
    font-weight: 700;
    min-width: 28px;
    text-align: right;
}

.pred-info {
    font-size: 9px;
    font-family: 'Space Mono', monospace;
    color: var(--accent2);
    text-align: center;
    margin-top: 9px;
}

/* RICH FAULT TOOLTIP */
.ftip {
    position: fixed;
    z-index: 9999;
    background: var(--surface);
    border: 1.5px solid #c7d2fe;
    border-radius: 14px;
    width: 310px;
    box-shadow: var(--sh-lg);
    opacity: 0;
    pointer-events: none;
    transition: opacity .18s, transform .18s;
    transform: translateY(4px);
}

.ftip.vis {
    opacity: 1;
    transform: translateY(0);
    pointer-events: auto;
}

.ft-head {
    padding: 12px 14px 10px;
    border-bottom: 1px solid var(--border);
    background: linear-gradient(90deg, #eef2ff, #f5f3ff);
    border-radius: 12px 12px 0 0;
}

.ft-htitle {
    font-size: 13px;
    font-weight: 700;
}

.ft-hsub {
    font-size: 9px;
    color: var(--muted);
    font-family: 'Space Mono', monospace;
    margin-top: 2px;
}

.ft-body {
    padding: 12px 14px;
}

.ft-sec {
    margin-bottom: 10px;
}

.ft-sec:last-child {
    margin-bottom: 0;
}

.ft-sec-t {
    font-size: 9px;
    font-weight: 700;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--muted2);
    font-family: 'Space Mono', monospace;
    margin-bottom: 5px;
}

.ft-row {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 4px;
    font-size: 10px;
}

.ft-key {
    color: var(--muted2);
}

.ft-val {
    font-family: 'Space Mono', monospace;
    font-weight: 700;
    font-size: 10px;
}

.ft-formula {
    background: var(--surface3);
    border-radius: 7px;
    padding: 8px 10px;
    font-family: 'Space Mono', monospace;
    font-size: 9px;
    color: var(--text2);
    line-height: 1.7;
    border: 1px solid var(--border);
    margin-top: 4px;
}

.ft-brow {
    margin-bottom: 5px;
}

.ft-blbl {
    display: flex;
    justify-content: space-between;
    font-size: 9px;
    color: var(--muted2);
    margin-bottom: 2px;
    font-family: 'Space Mono', monospace;
}

.ft-btrack {
    height: 6px;
    background: var(--border);
    border-radius: 3px;
    overflow: hidden;
}

.ft-bfill {
    height: 100%;
    border-radius: 3px;
    transition: width .5s ease;
}

.ft-foot {
    padding: 8px 14px;
    border-top: 1px solid var(--border);
    background: var(--surface3);
    border-radius: 0 0 12px 12px;
    font-size: 9px;
    color: var(--muted);
    font-family: 'Space Mono', monospace;
}

/* HEALTH RING */
.ring-wrap {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 10px;
    padding: 6px 0;
}

.ring-rel {
    position: relative;
    width: 130px;
    height: 130px;
}

.ring-inner {
    position: absolute;
    inset: 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

.ring-score {
    font-size: 32px;
    font-weight: 700;
    line-height: 1;
}

.ring-txt {
    font-size: 8px;
    color: var(--muted);
    font-family: 'Space Mono', monospace;
    letter-spacing: 1px;
    margin-top: 2px;
}

.gauge-row {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 8px;
    width: 100%;
}

.g-item {
    text-align: center;
}

.g-val {
    font-size: 13px;
    font-weight: 700;
}

.g-track {
    height: 5px;
    background: var(--border);
    border-radius: 3px;
    margin: 3px 0;
    overflow: hidden;
}

.g-fill {
    height: 100%;
    border-radius: 3px;
    transition: width 1.2s ease;
}

.g-lbl {
    font-size: 8px;
    color: var(--muted);
    font-family: 'Space Mono', monospace;
}

/* TEMP & NOISE */
.temp-big {
    font-size: 44px;
    font-weight: 700;
    line-height: 1;
}

.noise-bar {
    height: 8px;
    background: linear-gradient(90deg, #10b981, #f59e0b, #ef4444);
    border-radius: 4px;
    margin: 6px 0;
    position: relative;
}

.noise-pin {
    position: absolute;
    top: -5px;
    width: 16px;
    height: 16px;
    border-radius: 50%;
    background: #fff;
    border: 2.5px solid var(--text);
    transform: translateX(-50%);
    transition: left 1s ease;
    box-shadow: 0 2px 6px rgba(15, 23, 42, .2);
}

.spark-row {
    display: flex;
    align-items: flex-end;
    gap: 2px;
    height: 30px;
    margin-top: 4px;
}

.spark-b {
    flex: 1;
    border-radius: 2px 2px 0 0;
}

/* EVENTS */
.conn-list {
    display: flex;
    flex-direction: column;
    gap: 6px;
    margin-bottom: 12px;
}

.conn-item {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 7px 11px;
    background: var(--surface3);
    border-radius: 8px;
    font-size: 11px;
    border: 1px solid var(--border);
}

.conn-name {
    font-family: 'Space Mono', monospace;
    font-size: 9px;
    color: var(--muted2);
}

.ev-log {
    display: flex;
    flex-direction: column;
    gap: 5px;
    max-height: 150px;
    overflow-y: auto;
}

.ev-log::-webkit-scrollbar {
    width: 3px;
}

.ev-log::-webkit-scrollbar-thumb {
    background: var(--border2);
    border-radius: 2px;
}

.ev-item {
    display: flex;
    align-items: flex-start;
    gap: 8px;
    padding: 6px 9px;
    border-radius: 6px;
    background: var(--surface3);
    border: 1px solid var(--border);
    border-left-width: 2.5px;
    font-size: 10px;
}

.ev-time {
    font-family: 'Space Mono', monospace;
    font-size: 9px;
    color: var(--muted);
    white-space: nowrap;
}

footer {
    border-top: 1px solid var(--border);
    padding: 10px 28px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    font-size: 9px;
    color: var(--muted);
    font-family: 'Space Mono', monospace;
    max-width: 1680px;
    margin: 0 auto;
    background: var(--surface);
}

/* simple spec tip */
.stip {
    position: fixed;
    background: var(--surface);
    border: 1.5px solid var(--border);
    border-radius: 8px;
    padding: 6px 10px;
    font-size: 9px;
    font-family: 'Space Mono', monospace;
    pointer-events: none;
    opacity: 0;
    transition: opacity .15s;
    z-index: 8000;
    white-space: nowrap;
    box-shadow: var(--sh-md);
    color: var(--text2);
}

canvas {
    display: block;
}

::-webkit-scrollbar {
    width: 5px;
}

::-webkit-scrollbar-track {
    background: var(--bg);
}

::-webkit-scrollbar-thumb {
    background: var(--border2);
    border-radius: 3px;
}

@media(max-width:1200px) {
    .g-main {
        grid-template-columns: 1fr 1fr;
    }

    .kpi-row {
        grid-template-columns: repeat(3, 1fr);
    }
}

@media(max-width:800px) {
    .g-main {
        grid-template-columns: 1fr;
    }

    .g-bot {
        grid-template-columns: 1fr;
    }

    .kpi-row {
        grid-template-columns: repeat(2, 1fr);
    }
}
img{
    width:12vh !important
}
