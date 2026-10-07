# big-boss-2<!DOCTYPE html><html lang="en"><head><meta charset="utf-8"><meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover"><title>Big Boss Command Center</title>
<link rel="preconnect" href="https://fonts.googleapis.com"><link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@700;900&family=Rajdhani:wght@500;600;700&display=swap" rel="stylesheet">
<style>
:root{--bg:#141413;--pn:rgba(37,36,34,.74);--rd:#ff5a2e;--cy:#a5a58d;--gd:#f6b73c;--ok:#aab08f;--tx:#f8f6f0;--mu:#92927d;color-scheme:dark;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
*,*::before,*::after{box-sizing:inherit}html{scroll-padding-top:env(safe-area-inset-top,0px)}[hidden]{display:none!important}
body{margin:0;min-height:100vh;background:radial-gradient(900px 500px at 8% -10%,rgba(255,90,46,.2),transparent),radial-gradient(800px 500px at 100% 0,rgba(165,165,141,.13),transparent),#141413;background-attachment:fixed;color:var(--tx);font:600 15px/1.4 Rajdhani,system-ui,sans-serif;overflow-x:hidden}
body::before{content:"";position:fixed;inset:0;pointer-events:none;z-index:50;background:repeating-linear-gradient(0deg,rgba(255,255,255,.022) 0 1px,transparent 1px 3px)}
.wrap{max-width:1500px;margin:auto;padding:16px}
header{display:flex;justify-content:space-between;align-items:center;gap:12px;flex-wrap:wrap;padding:6px 4px}
h1{font:900 clamp(26px,4.6vw,52px)/1 Orbitron,Impact,sans-serif;letter-spacing:.06em;margin:0;text-shadow:0 0 24px rgba(255,90,46,.7)}h1 span{color:var(--rd)}
.sub{color:var(--cy);letter-spacing:.45em;font-size:12px;margin-top:8px}
.hr{display:flex;align-items:center;gap:14px;flex-wrap:wrap}#clk{color:var(--mu);font-size:14px}
.live{display:inline-flex;gap:8px;align-items:center;color:var(--rd);font:800 12px Orbitron,sans-serif;letter-spacing:.2em;border:1px solid var(--rd);padding:6px 12px;border-radius:99px;box-shadow:0 0 14px rgba(255,90,46,.4)}.live.sm{padding:3px 9px;font-size:10px}
.dot{width:9px;height:9px;border-radius:50%;background:var(--rd);box-shadow:0 0 10px var(--rd);animation:pulse 1.2s infinite}
@keyframes pulse{50%{opacity:.25;transform:scale(.7)}}@keyframes bl{50%{opacity:.3}}@keyframes fi{from{opacity:0}}@keyframes zi{from{transform:scale(.8);opacity:0}}
@keyframes glow{50%{box-shadow:0 0 34px rgba(255,90,46,.7)}}@keyframes fu{0%{background:rgba(170,176,143,.5)}}@keyframes fd{0%{background:rgba(255,90,46,.55)}}
.g{display:grid;gap:14px;margin-top:14px}.stats{grid-template-columns:repeat(auto-fit,minmax(150px,1fr))}
.r1{grid-template-columns:minmax(0,2fr) minmax(310px,1fr)}.r2{grid-template-columns:minmax(0,1.5fr) minmax(0,1fr)}.r3{grid-template-columns:repeat(4,minmax(0,1fr))}
@media(max-width:1200px){.r3{grid-template-columns:repeat(2,minmax(0,1fr))}}@media(max-width:900px){.r1,.r2,.r3{grid-template-columns:minmax(0,1fr)}}
.p{background:var(--pn);backdrop-filter:blur(12px);-webkit-backdrop-filter:blur(12px);border:1px solid rgba(255,90,46,.3);border-radius:14px;padding:14px;min-width:0;box-shadow:0 0 24px rgba(255,90,46,.08),inset 0 0 30px rgba(165,165,141,.04);transition:.2s}.p:hover{border-color:rgba(165,165,141,.55)}
.p>h2{margin:0 0 10px;font:800 13px Orbitron,sans-serif;letter-spacing:.18em;color:var(--cy);display:flex;align-items:center;justify-content:space-between;gap:8px}
h3{margin:14px 0 6px;font:800 11px Orbitron,sans-serif;letter-spacing:.2em;color:var(--mu);display:flex;justify-content:space-between}
.st{--c:var(--cy);border-top:2px solid var(--c)}.st.gd{--c:var(--gd)}.st.ok{--c:var(--ok)}.st.rd{--c:var(--rd)}.st.mu{--c:var(--mu)}
.st .l{color:var(--mu);font-size:11px;letter-spacing:.15em}.st .v{font:900 26px Orbitron,sans-serif;margin:4px 0;color:var(--c);white-space:nowrap;overflow:hidden;text-overflow:ellipsis;text-shadow:0 0 14px var(--c)}.st .s{color:var(--mu);font-size:13px}
button,select,input,textarea{font:inherit;color:var(--tx);background:rgba(255,255,255,.06);border:1px solid rgba(255,255,255,.16);border-radius:8px;padding:5px 9px;min-width:0}
option{background:#1e1d1b}button{cursor:pointer;font-weight:700;transition:.15s}button:hover{border-color:var(--cy);box-shadow:0 0 12px rgba(165,165,141,.45);transform:translateY(-1px)}
button.rd{background:linear-gradient(135deg,#ff5a2e,#c93a12);border-color:#ff8a63}button.rd:hover{box-shadow:0 0 16px rgba(255,90,46,.8)}
.gr{color:var(--ok)}.rb{color:#ff9a78}.gh{background:none}.chip{font-size:13px;padding:3px 9px;margin:3px 3px 0 0}.big{width:100%;margin-top:8px;padding:10px;font:800 14px Orbitron,sans-serif;letter-spacing:.1em}
textarea{width:100%;resize:vertical;min-height:58px}input[type=number]{width:72px}
.row2{display:flex;gap:8px;flex-wrap:wrap;align-items:center;margin:8px 0}.row2 input:not([type=number]),.row2 select{flex:1 1 120px}
.em{color:var(--mu);margin:6px 0}
.row{display:flex;align-items:center;gap:12px;padding:8px 12px;margin-bottom:6px;border-radius:10px;background:rgba(255,255,255,.03);border:1px solid rgba(255,255,255,.07)}
.rk{font:900 17px Orbitron,sans-serif;width:72px;color:var(--mu)}.nm{flex:1;min-width:0}.nm b{font-size:18px}.nm small{color:var(--mu);margin-left:8px}
.bar{height:4px;background:rgba(255,255,255,.09);border-radius:4px;margin-top:5px;overflow:hidden}.bar i{display:block;height:100%;background:linear-gradient(90deg,var(--cy),var(--rd));transition:width .6s}
.pt{font:800 20px Orbitron,sans-serif;min-width:64px;text-align:right}
.t1{border-color:#f6b73c;box-shadow:0 0 20px rgba(246,183,60,.35);background:linear-gradient(90deg,rgba(246,183,60,.16),transparent)}.t1 .rk{color:#f6b73c}
.t2{border-color:#a5a58d;box-shadow:0 0 14px rgba(165,165,141,.25)}.t2 .rk{color:#a5a58d}.t3{border-color:#cb997e;box-shadow:0 0 14px rgba(255,90,46,.25)}.t3 .rk{color:#cb997e}
.row.fu{animation:fu .9s}.row.fd{animation:fd .9s}
.bd{font:800 10px Orbitron,sans-serif;letter-spacing:.08em;padding:3px 8px;border-radius:99px;border:1px solid;white-space:nowrap;background:color-mix(in srgb,currentColor 12%,transparent)}
.sActive{color:var(--cy)}.sCaptain{color:var(--gd)}.sImmune{color:var(--ok)}.sNominated{color:var(--rd)}.sEvicted{color:var(--mu)}
.cap{text-align:center;padding:10px;border-radius:12px;background:radial-gradient(circle,rgba(246,183,60,.18),transparent 70%);border:1px solid rgba(246,183,60,.4)}
.cap .l{font:800 11px Orbitron,sans-serif;letter-spacing:.25em;color:var(--gd)}.crown{font-size:34px;filter:drop-shadow(0 0 10px #f8f6f0)}.cap b{display:block;font:900 26px Orbitron,sans-serif;color:var(--gd);text-shadow:0 0 18px rgba(246,183,60,.6)}.cap small{color:var(--mu)}
.td{font:900 clamp(40px,5.4vw,60px) Orbitron,sans-serif;text-align:center;letter-spacing:.06em;color:var(--cy);text-shadow:0 0 20px rgba(165,165,141,.6)}.td.up{color:var(--rd);text-shadow:0 0 26px var(--rd);animation:bl .6s infinite}
.tbar{height:5px;background:rgba(255,255,255,.09);border-radius:4px;overflow:hidden}.tbar i{display:block;height:100%;width:100%;background:var(--cy);transition:width .3s linear}
.tu{text-align:center;font:900 22px Orbitron,sans-serif;color:var(--rd);margin-top:6px;letter-spacing:.2em;animation:bl .6s infinite}
#cm2{max-height:660px;overflow:auto;padding-right:2px}.cr{padding:10px;margin-top:8px;border:1px solid rgba(255,255,255,.08);border-radius:10px;background:rgba(255,255,255,.025)}
.ch{display:flex;gap:10px;align-items:center;flex-wrap:wrap}.ch b{font-size:17px}.ch small{color:var(--mu)}.ch .pt{margin-left:auto;font-size:18px}
.ca{display:flex;gap:5px;flex-wrap:wrap;align-items:center;margin-top:8px}.ca input{width:64px}.sp{flex:1}
.tr{display:flex;flex-wrap:wrap;gap:8px;align-items:center;padding:8px 4px;border-bottom:1px solid rgba(255,255,255,.07)}.tr b{flex:1 1 140px}.tr select{max-width:150px}.tr.dn b{color:var(--mu);text-decoration:line-through}
.k{list-style:none;margin:0;padding:0}.k li{display:flex;align-items:center;gap:8px;padding:6px 0;border-bottom:1px solid rgba(255,255,255,.07)}.k li small{color:var(--mu);margin-left:auto}
.dz{counter-reset:n}.dz li::before{counter-increment:n;content:counter(n)".";font:800 16px Orbitron,sans-serif;color:var(--rd);width:26px}.dz li b{font-size:17px}
.hot{border-color:var(--rd);animation:glow 1.6s infinite}
.la q{display:block;font-size:17px;color:var(--gd);quotes:none}.la time{display:block;color:var(--mu);font-size:12px;margin:2px 0 8px}
.lg{max-height:230px;overflow:auto;font-size:14px}.lg time{color:var(--mu);margin-right:8px;font-size:12px}.lg .ann,.lg .warn{color:var(--gd)}.lg .err{color:#ff9a78}
#ov,#md{position:fixed;inset:0;display:none;place-items:center;padding:20px;background:rgba(0,0,0,.82);backdrop-filter:blur(6px)}#ov{z-index:100}#md{z-index:150}#ov.on,#md.on{display:grid;animation:fi .3s}
.ob{max-width:820px;width:100%;text-align:center;padding:34px 26px;border:2px solid var(--rd);border-radius:18px;background:rgba(38,28,23,.94);box-shadow:0 0 60px rgba(255,90,46,.6),inset 0 0 60px rgba(255,90,46,.15);animation:zi .5s}
.ob h3{justify-content:center;font-size:clamp(14px,2.4vw,24px);letter-spacing:.3em;color:var(--rd);margin:0 0 18px}.ob p{font:700 clamp(22px,3.4vw,38px)/1.3 Rajdhani,sans-serif;white-space:pre-wrap;margin:0 0 14px;overflow-wrap:anywhere}.ob time{color:var(--mu)}
.mb{background:#1e1d1b;border:1px solid var(--rd);border-radius:14px;padding:22px;text-align:center;box-shadow:0 0 40px rgba(255,90,46,.4);max-width:90vw}.mb p{font-size:20px;margin:0 0 16px}
#toasts{position:fixed;right:14px;bottom:calc(14px + env(safe-area-inset-bottom,0px));z-index:200;display:flex;flex-direction:column;max-width:calc(100vw - 28px)}
.ts{padding:10px 14px;margin-top:8px;border-radius:10px;background:#1e1d1b;border:1px solid var(--cy);box-shadow:0 0 16px rgba(165,165,141,.3);animation:fi .3s}.ts.err{border-color:var(--rd);box-shadow:0 0 16px rgba(255,90,46,.4)}.ts.warn{border-color:var(--gd)}
footer{text-align:center;margin:18px 0 6px}
@media(prefers-reduced-motion:reduce){*{animation:none!important;transition:none!important}}
#sc{position:fixed;inset:0;width:100%;height:100%;z-index:0;display:block}#vl{position:fixed;inset:0;z-index:0;pointer-events:none;background:linear-gradient(rgba(20,20,19,.2),rgba(20,20,19,.55))}.wrap{position:relative;z-index:1}
#vl{transition:opacity .8s}body.lp #vl{opacity:.3}
@keyframes lf{to{opacity:1}}@keyframes spin{to{transform:rotate(360deg)}}@keyframes scan{from{top:-120px}to{top:100%}}@keyframes lout{to{opacity:0;transform:scale(1.3);filter:blur(8px)}}@keyframes pgin{from{opacity:0;transform:translateY(16px)}}
@keyframes lti{from{opacity:0;transform:translateY(50px) scale(1.5);filter:blur(12px)}to{opacity:1;transform:none;filter:none}}@keyframes lsu{from{letter-spacing:1.2em;opacity:0}to{letter-spacing:.45em;opacity:1}}
.pgin{animation:pgin .5s cubic-bezier(.2,.8,.2,1)}
#nav{display:flex;gap:6px;flex-wrap:wrap;align-items:center;margin-top:10px;padding:6px;border:1px solid rgba(255,90,46,.3);border-radius:12px;background:var(--pn);backdrop-filter:blur(12px);-webkit-backdrop-filter:blur(12px)}
#nav a{padding:9px 14px;border-radius:8px;color:var(--mu);text-decoration:none;font:800 12px Orbitron,sans-serif;letter-spacing:.12em;transition:.2s}#nav a:hover{color:var(--tx);background:rgba(255,255,255,.07)}
#nav a.on{color:#fff;background:linear-gradient(135deg,rgba(255,90,46,.6),rgba(255,90,46,.15));box-shadow:0 0 14px rgba(255,90,46,.5)}
#nb:not(:empty){margin-left:6px;background:var(--rd);color:#fff;border-radius:99px;padding:1px 7px;animation:pulse 1.2s infinite}
body[data-r=contestants] .r2,body[data-r=tasks] .r2,body[data-r=dashboard] .r3,body[data-r=log] .r3{grid-template-columns:minmax(0,1fr)}
@media(min-width:1201px){body[data-r=danger] .r3{grid-template-columns:repeat(3,minmax(0,1fr))}}body[data-r=contestants] #cm2{max-height:none}
#land{position:fixed;inset:0;z-index:5;display:grid;place-items:center;text-align:center;padding:24px;overflow:hidden}#land.out{animation:lout .6s ease-in forwards}
.lc{position:relative;z-index:2;max-width:900px}.eb{opacity:0;animation:lf .8s .1s forwards}.eb .live{letter-spacing:.35em}
.lt{font:900 clamp(54px,12vw,150px)/.95 Orbitron,Impact,sans-serif;margin:16px 0 0;letter-spacing:.04em;text-shadow:0 0 40px rgba(255,90,46,.8),0 0 90px rgba(255,90,46,.4)}.lt i{font-style:normal;display:inline-block;opacity:0;animation:lti .8s cubic-bezier(.2,.8,.2,1) forwards}
.lsub{font:800 clamp(14px,2.4vw,24px) Orbitron,sans-serif;color:var(--rd);margin-top:10px;opacity:0;animation:lsu 1.4s 1.2s forwards}
.lp2{color:#d6d5c8;font-size:clamp(16px,2vw,20px);max-width:620px;margin:18px auto;opacity:0;animation:lf .9s 1.9s forwards}
.lbt{display:flex;gap:12px;justify-content:center;flex-wrap:wrap;opacity:0;animation:lf .9s 2.2s forwards}.lbt .big{width:auto;margin:0;padding:14px 26px}
.lst{display:flex;gap:10px;justify-content:center;flex-wrap:wrap;margin-top:24px;opacity:0;animation:lf .9s 2.6s forwards}
.lst span{border:1px solid rgba(165,165,141,.4);border-radius:10px;padding:8px 14px;background:var(--pn);font:800 11px Orbitron,sans-serif;letter-spacing:.12em;color:var(--cy)}.lst b{font-size:20px;color:var(--tx);margin-right:6px}
.ring{position:absolute;inset:0;display:grid;place-items:center;pointer-events:none}.ring svg{width:min(92vmin,840px);opacity:.55}.ring .a{animation:spin 40s linear infinite;transform-origin:100px 100px}.ring .b{animation:spin 26s linear infinite reverse;transform-origin:100px 100px}
.scan{position:absolute;left:0;right:0;height:120px;background:linear-gradient(transparent,rgba(165,165,141,.1),transparent);animation:scan 5s linear infinite;pointer-events:none}
.hero{margin-top:14px;display:grid;grid-template-columns:minmax(0,1fr) minmax(0,2fr);gap:14px 20px;align-items:center}
.hk{font:800 11px Orbitron,sans-serif;letter-spacing:.3em;color:var(--cy)}.ht{font:900 clamp(22px,3vw,34px) Orbitron,sans-serif;margin:6px 0;text-shadow:0 0 20px rgba(255,90,46,.5)}.hero p{margin:0;color:#d6d5c8}
.hs{display:grid;grid-template-columns:repeat(auto-fit,minmax(120px,1fr));gap:10px}.mini{padding:10px 12px;border:1px solid rgba(165,165,141,.3);border-radius:10px;background:rgba(255,255,255,.04)}.mini .l{color:var(--mu);font-size:11px;letter-spacing:.15em}.mini .v{font:900 22px Orbitron,sans-serif;color:var(--cy)}
.hx{grid-column:1/-1}.tb{display:flex;align-items:center;gap:10px;margin-top:6px}.tb span{min-width:110px;font:800 12px Orbitron,sans-serif;letter-spacing:.1em}.tb .bar{flex:1;height:8px;margin:0}.tb b{min-width:50px;text-align:right}
body[data-r=danger] .hero{border-color:var(--rd);box-shadow:0 0 30px rgba(255,90,46,.25)}body[data-r=danger] .mini .v{color:var(--rd)}body[data-r=tasks] .mini .v{color:var(--ok)}body[data-r=log] .mini .v{color:var(--gd)}
body[data-r=log] .r3{grid-template-columns:repeat(2,minmax(0,1fr))}body[data-r=log] .lg{max-height:520px}
.aq{border-left:3px solid var(--rd);padding:8px 12px;margin-bottom:10px;background:rgba(255,90,46,.06);border-radius:0 8px 8px 0}.aq q{display:block;font-size:18px;quotes:none}.aq time{color:var(--mu);font-size:12px}
@media(max-width:900px){.hero{grid-template-columns:minmax(0,1fr)}body[data-r=log] .r3{grid-template-columns:minmax(0,1fr)}}
button.rd{color:#252422}#nb:not(:empty){color:#252422}#nav a.on{color:#fff}.hero p,.lp2{color:#d6d5c8}
</style></head><body>
<canvas id="sc"></canvas><div id="vl"></div>
<section id="land" hidden><div class="ring"><svg viewBox="0 0 200 200" fill="none" stroke-width=".4"><g class="a" stroke="#ff5a2e"><circle cx="100" cy="100" r="96" stroke-dasharray="2 4"/><circle cx="100" cy="100" r="88" stroke-dasharray="40 12"/></g><g class="b" stroke="#a5a58d"><circle cx="100" cy="100" r="78" stroke-dasharray="1 3"/><circle cx="100" cy="100" r="70" stroke-dasharray="25 20"/></g></svg></div><div class="scan"></div>
<div class="lc"><div class="eb"><span class="live"><i class="dot"></i>HOUSE LIVE</span></div><h1 class="lt" id="lt"></h1><div class="lsub">COMMAND CENTER</div>
<p class="lp2">Total control of the Tech House. Contestants, tasks, nominations, immunity and evictions, all in real time.</p>
<div class="lbt"><button class="rd big" onclick="go('dashboard')">ENTER THE HOUSE ▶️</button><button class="big" onclick="go('contestants')">VIEW CONTESTANTS</button></div><div class="lst" id="ls"></div></div></section>
<div class="wrap" id="app" hidden>
<header><div><h1 onclick="go('landing')" style="cursor:pointer" title="Back to landing">BIG BOSS<span> COMMAND CENTER</span></h1><div class="sub">TECH HOUSE CONTROL SYSTEM</div></div><div class="hr"><span class="live"><i class="dot"></i>HOUSE LIVE</span><div id="clk"></div></div></header><nav id="nav"><a href="#/dashboard" onclick="go('dashboard');return false">🏠 COMMAND CENTER</a><a href="#/contestants" onclick="go('contestants');return false">👥 CONTESTANTS</a><a href="#/tasks" onclick="go('tasks');return false">📋 TASKS</a><a href="#/danger" onclick="go('danger');return false">⚠ DANGER ZONE<b id="nb"></b></a><a href="#/log" onclick="go('log');return false">📢 ANNOUNCEMENTS &amp; LOG</a><a href="#/landing" onclick="go('landing');return false" style="margin-left:auto">⟵ LANDING</a></nav>
<section class="p hero" id="hero" data-p="contestants tasks danger log"></section>
<section class="g stats" id="stats" data-p="dashboard"></section>
<section class="g r1" data-p="dashboard">
<div class="p"><h2><span>LIVE RANKINGS</span><span class="live sm"><i class="dot"></i>LIVE</span></h2><div id="lb"></div></div>
<div class="p"><h2>HOUSE CONTROL</h2>
<div class="cap"><div class="l">HOUSE CAPTAIN</div><div class="crown">👑</div><b id="cn"></b><small id="cs"></small></div>
<div class="row2"><select id="fc"></select><button onclick="cap($('fc').value)">Appoint Captain</button><button class="gh" onclick="uncap()">Remove</button></div>
<h3>TASK TIMER <span id="tst"></span></h3><div id="td" class="td">05:00</div><div class="tbar"><i id="tb"></i></div><div id="tu" class="tu" hidden>⏰ TIME UP</div>
<div class="row2"><input id="tm" type="number" min="0" max="99" value="5" oninput="tset()"> min <input id="tsec" type="number" min="0" max="59" value="0" oninput="tset()"> sec</div>
<div class="row2"><button class="gr" onclick="tstart()">▶️ Start</button><button onclick="tpause()">⏸ Pause</button><button class="rb" onclick="treset()">⟲ Reset</button></div>
<h3>QUICK ANNOUNCEMENT</h3><textarea id="an" placeholder="Attention Housemates. The task begins NOW."></textarea><button class="rd big" onclick="ann()">📢 BIG BOSS ANNOUNCEMENT</button>
</div></section>
<section class="g r2" data-p="contestants tasks">
<div class="p" data-p="contestants"><h2>CONTESTANT MANAGEMENT</h2>
<div class="row2"><input id="fn" placeholder="Name"><input id="ft" list="tms" placeholder="Team"><datalist id="tms"><option value="Titans"><option value="Mavericks"></datalist><input id="fp" type="number" placeholder="Pts" value="100"><button class="gr" onclick="addC()">＋ Add Contestant</button></div>
<div id="cm2"></div><h3>🚪 EVICTION HISTORY</h3><div id="eh"></div></div>
<div class="p" data-p="tasks"><h2>TASK MANAGEMENT</h2>
<div class="row2"><input id="tn" placeholder="New task name"><select id="tw"></select><button class="gr" onclick="addT()">＋ Add Task</button></div><div id="tl"></div></div>
</section>
<section class="g r3" data-p="dashboard danger log">
<div class="p" id="dzp" data-p="dashboard danger"><h2 style="color:var(--rd)">⚠ DANGER ZONE</h2><div id="dz"></div></div>
<div class="p" data-p="danger"><h2>NOMINATIONS</h2><div class="row2"><select id="fn2"></select><button class="rd" onclick="nom($('fn2').value)">⚠ NOMINATE</button></div><p class="em">Quick nominate (immune contestants and the Captain are protected):</p><div id="nl"></div></div>
<div class="p" data-p="danger"><h2>🛡 IMMUNITY</h2><div class="row2"><select id="fi"></select><button class="gr" onclick="imm($('fi').value)">🛡 Grant Immunity</button></div><div id="il"></div></div>
<div class="p" data-p="log"><h2>📢 ANNOUNCEMENT HISTORY</h2><div id="ah"></div></div>
<div class="p" data-p="log"><h2>EVENT LOG</h2><div id="la" class="la"></div><ul id="lg" class="k lg"></ul></div>
</section>
<footer><button class="gh" onclick="resetH()">⟲ Reset demo data</button></footer>
</div>
<div id="ov" onclick="this.classList.remove('on')"><div class="ob"><h3>📢 BIG BOSS ANNOUNCEMENT</h3><p id="om"></p><time id="od"></time></div></div>
<div id="md"><div class="mb"><p id="cm"></p><button class="rd" onclick="yes(1)">Confirm</button> <button onclick="yes(0)">Cancel</button></div></div>
<div id="toasts"></div>
<script>
const $=id=>document.getElementById(id),esc=s=>String(s).replace(/[&<>"']/g,m=>'&#'+m.charCodeAt(0)+';');
const K='bigboss.v1',B={Active:'ACTIVE',Captain:'👑 CAPTAIN',Immune:'🛡 IMMUNE',Nominated:'⚠ NOMINATED',Evicted:'EVICTED'};
const badge=c=>`<span class="bd s${c.st}">${B[c.st]}</span>`,now=()=>new Date().toLocaleTimeString();
const seed=()=>({c:[['Aarav','Titans',850],['Riya','Titans',720],['Kabir','Mavericks',690],['Ananya','Mavericks',640],['Vihaan','Titans',590],['Meera','Mavericks',530],['Arjun','Titans',480],['Ishita','Mavericks',420]].map((a,i)=>({id:i+1,name:a[0],team:a[1],pts:a[2],st:'Active'})),
t:[['Team Cooking Challenge',2,0],['Memory Maze',3,1],['Strategy Mission',4,0],['Tech Puzzle',5,1],['Treasure Hunt',6,0]].map((a,i)=>({id:i+1,name:a[0],who:a[1],done:!!a[2]})),log:[],last:null,nid:100});
let S,FL={},cb,ot,dur=300,left=300,end=0,iv=0,fin=false;
try{S=JSON.parse(localStorage.getItem(K))}catch(e){}
if(!S||!S.c)S=seed();
const g=id=>S.c.find(x=>x.id==id);
function save(){try{localStorage.setItem(K,JSON.stringify(S))}catch(e){}}
function commit(){save();render()}
function toast(m,k='ok'){const d=document.createElement('div');d.className='ts '+k;d.textContent=m;$('toasts').append(d);setTimeout(()=>d.remove(),3200)}
function ev(m,k='ok',lg=m){toast(m,k);S.log.unshift({t:now(),m:lg,k});S.log.length=Math.min(S.log.length,40);commit()}
function ask(m,f){cb=f;$('cm').textContent=m;$('md').classList.add('on')}
function yes(ok){$('md').classList.remove('on');const f=cb;cb=null;if(ok&&f)f()}
function pts(id,n){const c=g(id);if(!c||c.st=='Evicted')return toast('Evicted contestants cannot receive points','err');n=Math.round(n);if(!n)return;c.pts=Math.max(0,c.pts+n);FL[id]=n>0?'fu':'fd';ev(n>0?`✓ ${n} points added to ${c.name}`:`➖ ${-n} points deducted from ${c.name}`,n>0?'ok':'warn')}
function cus(id){const v=+$('cu'+id).value;if(!v)return toast('Enter a non-zero amount (negative deducts)','err');pts(id,v)}
function cap(id){const c=g(id);if(!c||id==0)return toast('Select a contestant first','err');if(c.st=='Evicted')return toast(`🚨 ${c.name} is evicted and cannot be Captain`,'err');if(c.st!='Active')return toast(`${c.name} is ${c.st} — only Active contestants can be Captain`,'err');S.c.forEach(x=>{if(x.st=='Captain')x.st='Active'});c.st='Captain';ev(`👑 ${c.name} is now House Captain`)}
function uncap(){const c=S.c.find(x=>x.st=='Captain');if(!c)return toast('There is no Captain to remove','warn');c.st='Active';ev(`${c.name} is no longer House Captain`,'warn')}
function nom(id){const c=g(id);if(!c||id==0)return toast('Select a contestant first','err');if(c.st=='Evicted')return toast(`🚨 ${c.name} is evicted and cannot be nominated`,'err');if(c.st=='Immune')return toast(`🛡 ${c.name} is IMMUNE and cannot be nominated`,'err');if(c.st=='Captain')return toast(`👑 ${c.name} is House Captain and cannot be nominated`,'err');if(c.st=='Nominated')return toast(`${c.name} is already nominated`,'warn');c.st='Nominated';ev(`⚠ ${c.name} has been nominated`,'warn')}
function unnom(id){const c=g(id);if(c&&c.st=='Nominated'){c.st='Active';ev(`${c.name} removed from the Danger Zone`)}}
function imm(id){const c=g(id);if(!c||id==0)return toast('Select a contestant first','err');if(c.st=='Evicted')return toast(`${c.name} is evicted`,'err');if(c.st=='Captain')return toast(`👑 ${c.name} is Captain — remove captaincy first`,'err');if(c.st=='Immune'){c.st='Active';return ev(`${c.name} immunity removed`,'warn')}const was=c.st=='Nominated';c.st='Immune';ev(`🛡 ${c.name} is now immune`,'ok',`🛡 ${c.name} is now immune`+(was?' (nomination cleared)':''))}
function evict(id){const c=g(id);if(!c||c.st=='Evicted')return;ask(`Evict ${c.name}? This cannot be undone.`,()=>{c.st='Evicted';c.at=new Date().toLocaleString();S.t.forEach(t=>{if(t.who==c.id&&!t.done)t.who=0});ev(`🚨 ${c.name} has been evicted`,'err')})}
function addC(){const n=$('fn').value.trim();if(!n)return toast('Enter a contestant name','err');if(S.c.some(x=>x.name.toLowerCase()==n.toLowerCase()))return toast(`${n} is already in the House`,'err');S.c.push({id:S.nid++,name:n,team:$('ft').value.trim()||'Titans',pts:Math.max(0,+$('fp').value||0),st:'Active'});$('fn').value='';ev(`➕ ${n} entered the House`)}
function addT(){const n=$('tn').value.trim(),w=+$('tw').value;if(!n)return toast('Enter a task name','err');const c=g(w);if(w&&(!c||c.st=='Evicted'))return toast('Evicted contestants cannot receive tasks','err');S.t.unshift({id:S.nid++,name:n,who:w,done:false});$('tn').value='';ev(`📋 Task "${n}" created`+(c?` for ${c.name}`:''))}
function reT(id,w){const t=S.t.find(x=>x.id==id),c=g(w);if(!t)return;if(+w&&(!c||c.st=='Evicted'))return toast('Evicted contestants cannot receive tasks','err');t.who=+w;ev(c?`📋 "${t.name}" assigned to ${c.name}`:`"${t.name}" is now unassigned`)}
function doneT(id){const t=S.t.find(x=>x.id==id);if(!t)return;const c=g(t.who);if(!c||c.st=='Evicted')return toast('Assign this task to an active contestant first','err');t.done=true;ev(`✅ "${t.name}" completed by ${c.name}`)}
function ann(){const v=$('an').value.trim();if(!v)return toast('Type an announcement first','err');S.last={m:v,t:new Date().toLocaleString()};$('an').value='';$('om').textContent=v;$('od').textContent=S.last.t;$('ov').classList.add('on');clearTimeout(ot);ot=setTimeout(()=>$('ov').classList.remove('on'),8000);ev('📢 Announcement broadcasted','ann','📢 '+v)}
function resetH(){ask('Reset the whole House to demo data?',()=>{S=seed();FL={};commit();toast('House reset to demo data','warn')})}
const mmss=s=>String(Math.floor(s/60)).padStart(2,'0')+':'+String(s%60).padStart(2,'0');
function tdraw(){const up=fin&&!iv;$('td').textContent=mmss(left);$('td').classList.toggle('up',up);$('tu').hidden=!up;$('tb').style.width=(left/dur*100)+'%';$('tst').textContent=up?'TIME UP':iv?'● RUNNING':left<dur?'❚❚ PAUSED':'READY'}
function tset(){if(iv)return;dur=Math.max(1,(+$('tm').value||0)*60+(+$('tsec').value||0));left=dur;fin=false;tdraw()}
function tstart(){if(iv)return;if(left<=0)left=dur;fin=false;end=Date.now()+left*1000;iv=setInterval(()=>{left=Math.max(0,Math.ceil((end-Date.now())/1000));if(!left){clearInterval(iv);iv=0;fin=true;tdraw();ev('⏰ TIME UP — the task timer has ended','err')}else tdraw()},200);tdraw();toast('▶️ Timer started')}
function tpause(){if(!iv)return toast('Timer is not running','warn');clearInterval(iv);iv=0;tdraw();toast('⏸ Timer paused','warn')}
function treset(){clearInterval(iv);iv=0;tset();toast('⟲ Timer reset','warn')}
function fill(id,a,ph){const s=$(id),v=s.value;s.innerHTML=`<option value="0">${ph}</option>`+a.map(c=>`<option value="${c.id}">${esc(c.name)} — ${c.st}</option>`).join('');s.value=v;if(s.value!=v)s.value='0'}
function render(){
const A=S.c.filter(x=>x.st!='Evicted'),L=[...A].sort((a,b)=>b.pts-a.pts||a.name.localeCompare(b.name)),top=Math.max(1,L[0]?L[0].pts:1);
const by=s=>S.c.filter(x=>x.st==s),N=by('Nominated'),I=by('Immune'),E=by('Evicted'),C=by('Captain')[0],D=S.t.filter(x=>x.done).length;
const old={};document.querySelectorAll('#lb .row').forEach(e=>old[e.dataset.id]=e.getBoundingClientRect().top);
$('lb').innerHTML=L.length?L.map((c,i)=>`<div class="row t${i<3?i+1:0} ${FL[c.id]||''}" data-id="${c.id}"><div class="rk">#${i+1}${['🥇','🥈','🥉'][i]||''}</div><div class="nm"><b>${esc(c.name)}</b><small>${esc(c.team)}</small><div class="bar"><i style="width:${c.pts/top*100}%"></i></div></div>${badge(c)}<div class="pt">${c.pts}</div></div>`).join(''):'<p class="em">No active contestants.</p>';
document.querySelectorAll('#lb .row').forEach(e=>{const o=old[e.dataset.id];if(o!=null){const d=o-e.getBoundingClientRect().top;if(d)e.animate([{transform:`translateY(${d}px)`},{transform:'none'}],{duration:450,easing:'cubic-bezier(.2,.8,.2,1)'})}});
const stat=(l,v,s,c)=>`<div class="p st ${c}"><div class="l">${l}</div><div class="v">${v}</div><div class="s">${s}</div></div>`;
$('stats').innerHTML=stat('ACTIVE CONTESTANTS',L.length,'in the House','cy')+stat('HIGHEST SCORER',L[0]?esc(L[0].name):'—',L[0]?L[0].pts+' pts':'','gd')+stat('COMPLETED TASKS',D,`<div class="bar"><i style="width:${S.t.length?D/S.t.length*100:0}%"></i></div>${S.t.length-D} pending`,'ok')+stat('NOMINEES',N.length,'in danger','rd')+stat('IMMUNE',I.length,'protected','ok')+stat('EVICTED',E.length,'gone','mu')+stat('CAPTAIN',C?esc(C.name):'—','House Captain','gd');
$('cn').textContent=C?C.name:'— VACANT —';$('cs').textContent=C?`${C.team} · ${C.pts} pts`:'No captain appointed';
fill('fc',A.filter(x=>x.st=='Active'),'Select eligible contestant…');fill('fn2',A,'Select contestant…');fill('fi',A.filter(x=>x.st=='Active'||x.st=='Nominated'),'Select contestant…');fill('tw',A,'Unassigned');
$('cm2').innerHTML=A.map(c=>`<div class="cr"><div class="ch"><b>${esc(c.name)}</b><small>${esc(c.team)}</small>${badge(c)}<span class="pt">${c.pts}</span></div><div class="ca">${[10,25,50].map(n=>`<button class="gr" onclick="pts(${c.id},${n})">+${n}</button>`).join('')}${[10,25,50].map(n=>`<button class="rb" onclick="pts(${c.id},-${n})">−${n}</button>`).join('')}<input id="cu${c.id}" type="number" placeholder="±pts" title="Custom: positive adds, negative deducts"><button onclick="cus(${c.id})">Apply</button><i class="sp"></i><button onclick="cap(${c.id})">👑 Captain</button><button onclick="nom(${c.id})">⚠ Nominate</button><button onclick="imm(${c.id})">🛡 ${c.st=='Immune'?'Remove Immunity':'Immunity'}</button><button class="rd" onclick="evict(${c.id})">🚨 Evict</button></div></div>`).join('')||'<p class="em">No active contestants.</p>';
$('eh').innerHTML=E.length?E.map(c=>`<span class="bd sEvicted chip">🚪 ${esc(c.name)} · ${esc(c.team)} · ${c.pts} pts${c.at?' · '+esc(c.at):''}</span>`).join(' '):'<p class="em">No evictions yet.</p>';
$('tl').innerHTML=S.t.map(t=>{const c=g(t.who);return `<div class="tr ${t.done?'dn':''}"><b>${esc(t.name)}</b>${t.done?`<span>${c?esc(c.name):'—'}</span>`:`<select onchange="reT(${t.id},this.value)"><option value="0">Unassigned</option>${A.map(a=>`<option value="${a.id}"${a.id==t.who?' selected':''}>${esc(a.name)}</option>`).join('')}</select>`}<span class="bd ${t.done?'sImmune':'sNominated'}">${t.done?'✓ COMPLETED':'… PENDING'}</span>${t.done?'':`<button class="gr" onclick="doneT(${t.id})">✔ Complete</button>`}</div>`}).join('')||'<p class="em">No tasks yet.</p>';
$('dz').innerHTML=N.length?`<ol class="k dz">${N.map(c=>`<li><b>${esc(c.name)}</b><small>${esc(c.team)} · ${c.pts} pts</small><button class="gh" onclick="unnom(${c.id})">Clear</button></li>`).join('')}</ol>`:'<p class="em">No contestants currently nominated.</p>';
$('dzp').classList.toggle('hot',N.length>0);
$('nl').innerHTML=A.filter(x=>x.st=='Active').map(c=>`<button class="chip" onclick="nom(${c.id})">⚠ ${esc(c.name)}</button>`).join('')||'<p class="em">No eligible contestants.</p>';
$('il').innerHTML=I.length?`<ul class="k">${I.map(c=>`<li>🛡 <b>${esc(c.name)}</b><small>${esc(c.team)}</small><button class="gh" onclick="imm(${c.id})">Remove</button></li>`).join('')}</ul>`:'<p class="em">Nobody is immune.</p>';
$('la').innerHTML=S.last?`<q>${esc(S.last.m)}</q><time>${esc(S.last.t)}</time>`:'<p class="em">No announcements yet.</p>';
$('lg').innerHTML=S.log.map(l=>`<li class="${l.k||''}"><span><time>${esc(l.t)}</time>${esc(l.m)}</span></li>`).join('')||'<li class="em">No events yet.</li>';
const sum=L.reduce((a,c)=>a+c.pts,0),T={};L.forEach(c=>T[c.team]=(T[c.team]||0)+c.pts);const tm=Object.entries(T).sort((a,b)=>b[1]-a[1]),tmx=Math.max(1,...tm.map(a=>a[1])),pc=S.t.length?Math.round(D/S.t.length*100):0,an=S.log.filter(x=>x.k=='ann');
const m=(l,v)=>`<div class="mini"><div class="l">${l}</div><div class="v">${v}</div></div>`,bar=(a,w,b)=>`<div class="tb"><span>${a}</span><div class="bar"><i style="width:${w}%"></i></div><b>${b}</b></div>`;
const H={contestants:['02','👥 CONTESTANT ROSTER','Adjust points, appoint the Captain, nominate, grant immunity or evict.',m('IN THE HOUSE',L.length)+m('TOTAL POINTS',sum)+m('AVERAGE',L.length?Math.round(sum/L.length):0)+m('LEADING TEAM',tm[0]?esc(tm[0][0]):'—'),tm.map(a=>bar(esc(a[0]),a[1]/tmx*100,a[1])).join('')],
tasks:['03','📋 TASK BOARD','Create challenges, assign them to active housemates and mark them complete.',m('TOTAL TASKS',S.t.length)+m('COMPLETED',D)+m('PENDING',S.t.length-D)+m('PROGRESS',pc+'%'),bar('HOUSE PROGRESS',pc,pc+'%')],
danger:['04','⚠ DANGER ZONE','Nominate housemates and manage immunity. Immune contestants cannot be nominated.',m('NOMINEES',N.length)+m('IMMUNE',I.length)+m('ELIGIBLE',A.filter(x=>x.st=='Active').length)+m('EVICTED',E.length),N.length?`<div class="tb"><span>🚨 AT RISK</span><b style="flex:1;text-align:left;color:var(--rd)">${N.map(c=>esc(c.name)).join(' · ')}</b></div>`:''],
log:['05','📢 BROADCAST ARCHIVE','Every announcement and House event, newest first.',m('ANNOUNCEMENTS',an.length)+m('EVENTS LOGGED',S.log.length)+m('LAST EVENT',S.log[0]?esc(S.log[0].t):'—')+m('CAPTAIN',C?esc(C.name):'—'),'']}[cur];
$('hero').innerHTML=H?`<div><div class="hk">PAGE ${H[0]} / 05</div><div class="ht">${H[1]}</div><p>${H[2]}</p></div><div class="hs">${H[3]}</div>${H[4]?`<div class="hx">${H[4]}</div>`:''}`:'';
$('ah').innerHTML=an.length?an.map(a=>`<div class="aq"><q>${esc(a.m.replace(/^📢 /,''))}</q><time>${esc(a.t)}</time></div>`).join(''):'<p class="em">No announcements yet.</p>';
$('nb').textContent=N.length||'';$('ls').innerHTML=[[L.length,'HOUSEMATES'],[N.length,'NOMINEES'],[D,'TASKS DONE']].map(a=>`<span><b>${a[0]}</b>${a[1]}</span>`).join('');
FL={}}
setInterval(()=>$('clk').textContent=new Date().toLocaleString([],{weekday:'short',day:'2-digit',month:'short',hour:'2-digit',minute:'2-digit',second:'2-digit'}),1000);
$('clk').textContent=new Date().toLocaleString();
const PG=['landing','dashboard','contestants','tasks','danger','log'];let cur='landing';
const hp=()=>{const r=(location.hash.match(/^#\/(\w+)/)||[])[1];return PG.includes(r)?r:'landing'};
function go(p){if(p==cur)return;if(cur!='landing'||p=='landing')return route(p);$('land').classList.add('out');window.CZ=6;setTimeout(()=>route(p),550)}
function route(r){cur=r;try{if(hp()!=r)location.hash='#/'+r}catch(e){}
document.body.dataset.r=r;document.body.classList.toggle('lp',r=='landing');$('land').hidden=r!='landing';$('app').hidden=r=='landing';
document.querySelectorAll('[data-p]').forEach(e=>e.hidden=!e.dataset.p.split(' ').includes(r));document.querySelectorAll('#nav a').forEach(a=>a.classList.toggle('on',a.getAttribute('href')=='#/'+r));window.CZ=r=='landing'?22:34;
if(r=='landing'){$('land').classList.remove('out');$('lt').innerHTML=[...'BIG BOSS'].map((c,i)=>`<i style="animation-delay:${.3+i*.09}s">${c==' '?'&nbsp;':c}</i>`).join('')}
else{const a=$('app');a.classList.remove('pgin');void a.offsetWidth;a.classList.add('pgin');scrollTo(0,0)}render()}
addEventListener('hashchange',()=>{const r=hp();if(r!=cur)route(r)});tset();route(hp());
</script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
<script>
(()=>{try{
const R=new THREE.WebGLRenderer({canvas:$('sc'),antialias:true}),sc=new THREE.Scene(),cam=new THREE.PerspectiveCamera(50,1,.1,500),V=THREE.Vector3,rnd=Math.random;
R.setPixelRatio(Math.min(devicePixelRatio,1.5));sc.background=new THREE.Color(0x151412);sc.fog=new THREE.FogExp2(0x1d1c18,.011);
const rs=()=>{R.setSize(innerWidth,innerHeight,false);cam.aspect=innerWidth/innerHeight;cam.updateProjectionMatrix()};addEventListener('resize',rs);rs();
const k=document.createElement('canvas');k.width=k.height=64;const x2=k.getContext('2d'),gr=x2.createRadialGradient(32,32,0,32,32,32);gr.addColorStop(0,'rgba(255,255,255,1)');gr.addColorStop(1,'rgba(255,255,255,0)');x2.fillStyle=gr;x2.fillRect(0,0,64,64);const G=new THREE.CanvasTexture(k);
const spr=(c,s,x,y,z,o,add=true)=>{const m=new THREE.Sprite(new THREE.SpriteMaterial({map:G,color:c,transparent:true,opacity:o,depthWrite:false,fog:false,blending:add?THREE.AdditiveBlending:THREE.NormalBlending}));m.scale.set(s,s,1);m.position.set(x,y,z);sc.add(m);return m};
const std=(c,r=.8,m=0)=>new THREE.MeshStandardMaterial({color:c,roughness:r,metalness:m}),RF=std(0x26281f,.45,.2),WD=std(0x3d2e25),RD=std(0xe0522b,.6),ST=std(0x34352c),WN=new THREE.MeshBasicMaterial({color:0xffc46b});
const add=(g,m,x,y,z)=>{const o=new THREE.Mesh(g,m);o.position.set(x,y,z);sc.add(o);return o};
const bx=(w,h,d,m,x,y,z)=>add(new THREE.BoxGeometry(w,h,d),m,x,y,z),cy=(r,h,m,x,y,z)=>add(new THREE.CylinderGeometry(r,r,h,8),m,x,y,z),pl=(w,h,x,y,z)=>add(new THREE.PlaneGeometry(w,h),WN,x,y,z);
const cg=new THREE.ConeGeometry(1,1,4);cg.rotateY(Math.PI/4);const roof=(w,h,d,x,y,z)=>{const o=add(cg,RF,x,y+h/2,z);o.scale.set(w/1.4142,h,d/1.4142)};
spr(0xa5a58d,50,-26,30,-130,.55);add(new THREE.SphereGeometry(3.4,24,16),new THREE.MeshBasicMaterial({color:0xf8f6f0,fog:false}),-26,30,-130);
{const p=[];for(let i=0;i<350;i++)p.push((rnd()-.5)*400,20+rnd()*110,-180);const g=new THREE.BufferGeometry();g.setAttribute('position',new THREE.Float32BufferAttribute(p,3));sc.add(new THREE.Points(g,new THREE.PointsMaterial({size:1.6,sizeAttenuation:false,color:0xf8f6f0,fog:false})))}
const mt=(z,h,c,s)=>{const sh=new THREE.Shape();sh.moveTo(-170,-10);for(let i=0;i<=42;i++)sh.lineTo(-170+i*8,h*(.55+.3*Math.sin(i*.55+s)+.15*Math.sin(i*1.37+s*2)));sh.lineTo(170,-10);add(new THREE.ShapeGeometry(sh),new THREE.MeshBasicMaterial({color:c}),0,0,z)};
mt(-95,38,0x34372a,1);mt(-75,28,0x282b20,3);mt(-55,18,0x1c1e17,5);
const gd=add(new THREE.PlaneGeometry(500,500),std(0x10100d,.25,.3),0,0,0);gd.rotation.x=-Math.PI/2;
bx(32,1,22,ST,0,.5,0);bx(6,.06,23,std(0x3a3b31),0,.03,22.5);
for(let i=0;i<5;i++){const s=7-i*1.05,y=1+i*3.5;bx(s*.62,2.2,s*.62,WD,-10,y+1.1,-3);bx(s*1.05,.2,s*1.05,RD,-10,y+2.2,-3);roof(s*1.5,1.5,s*1.5,-10,y+2.2,-3);for(const d of[-.18,.18])pl(s*.12,1,-10+d*s,y+1.1,-3+s*.31+.02)}
cy(.12,3,RD,-10,20,-3);spr(0xffc46b,3,-10,21.8,-3,.8);
bx(14,4,8,WD,7,3,0);for(let i=0;i<7;i++)cy(.28,4,RD,1+i*2,3,4.3);bx(15,.4,9.4,RD,7,5.1,0);roof(19,5,12,7,5.2,0);roof(11,3,6.5,7,9.6,0);for(let i=0;i<3;i++)pl(3,2.2,3.5+i*3.5,3,4.02);spr(0xff9a4a,16,7,3.5,4.5,.2);
for(const s of[-1,1])cy(.35,7.5,RD,s*3.4,3.75,12);bx(10.8,.5,.8,RF,0,7.6,12);bx(8,.35,.4,RD,0,6.4,12);
for(const[x,z]of[[-5,17],[5,17],[-5,23],[5,23]]){bx(.5,1.3,.5,ST,x,.65,z);bx(.9,.8,.9,WN,x,1.7,z);bx(1.2,.25,1.2,ST,x,2.2,z);spr(0xff9a4a,4,x,1.7,z,.6)}
sc.add(new THREE.HemisphereLight(0x80846b,0x0c0c0a,.55));const ml=new THREE.DirectionalLight(0xe6e4d6,.8);ml.position.set(-26,30,-60);sc.add(ml);const fl=new THREE.DirectionalLight(0x959880,.35);fl.position.set(8,14,40);sc.add(fl);
for(const a of[[-5,3,17,1.4],[5,3,17,1.4],[7,3.5,5,2.2]]){const l=new THREE.PointLight(0xff9a4a,a[3],26,1.6);l.position.set(a[0],a[1],a[2]);sc.add(l)}
const N=1400,rp=new Float32Array(N*6),hx=[],hy=[],hz=[],sp=[],rg=new THREE.BufferGeometry();for(let i=0;i<N;i++){hx.push((rnd()-.5)*90);hy.push(rnd()*50);hz.push(rnd()*80-40);sp.push(30+rnd()*20)}
rg.setAttribute('position',new THREE.BufferAttribute(rp,3));const rain=new THREE.LineSegments(rg,new THREE.LineBasicMaterial({color:0xa5a58d,transparent:true,opacity:.35}));rain.frustumCulled=false;sc.add(rain);
const Ms=[];for(let i=0;i<8;i++){const m=spr(0x6b705c,1,0,2+rnd()*3,rnd()*60-30,.11,false);m.scale.set(48,10,1);Ms.push({m,x:(i-4)*14,p:rnd()*6})}
const NL=110,lp=new Float32Array(NL*3),lc=new Float32Array(NL*3),lph=[],lg=new THREE.BufferGeometry();for(let i=0;i<NL;i++){lp.set([(rnd()-.5)*60,rnd()*20,rnd()*50-15],i*3);lc.set([.9+rnd()*.1,.35+rnd()*.35,.1+rnd()*.1],i*3);lph.push(rnd()*6.28)}
lg.setAttribute('position',new THREE.BufferAttribute(lp,3));lg.setAttribute('color',new THREE.BufferAttribute(lc,3));const lv=new THREE.Points(lg,new THREE.PointsMaterial({size:.45,map:G,vertexColors:true,transparent:true,depthWrite:false,opacity:.9}));lv.frustumCulled=false;sc.add(lv);
const W=[];for(let i=0;i<12;i++)W.push({s:spr(0xa5a58d,1,0,-99,0,0),l:0,v:new V});let wi=0,lw=0,mx=0,my=0;const pv=new V,rd=new V;
addEventListener('pointermove',e=>{mx=e.clientX/innerWidth*2-1;my=-(e.clientY/innerHeight*2-1);const n=performance.now();if(n-lw<90)return;lw=n;pv.set(mx,my,.5).unproject(cam);rd.copy(pv).sub(cam.position).normalize();const w=W[wi++%W.length];w.s.position.copy(cam.position).addScaledVector(rd,(10-cam.position.z)/rd.z);w.l=1;w.v.set((rnd()-.5)*.6,rnd()*.5+.2,0)});
let t=0,t0=performance.now();const tick=()=>{requestAnimationFrame(tick);const n=performance.now(),dt=Math.min(.05,(n-t0)/1000);t0=n;t+=dt;
for(let i=0;i<N;i++){hy[i]-=sp[i]*dt;if(hy[i]<0)hy[i]=50;const j=i*6;rp[j]=hx[i];rp[j+1]=hy[i];rp[j+2]=hz[i];rp[j+3]=hx[i]+.12;rp[j+4]=hy[i]+1;rp[j+5]=hz[i]}rg.attributes.position.needsUpdate=true;
for(let i=0;i<NL;i++){const j=i*3;lp[j+1]-=.9*dt;lp[j]+=(Math.sin(t*.8+lph[i])*.6+.4)*dt;lp[j+2]+=Math.cos(t*.6+lph[i])*.3*dt;if(lp[j+1]<0){lp[j+1]=20;lp[j]=(rnd()-.5)*60}}lg.attributes.position.needsUpdate=true;
for(const o of Ms)o.m.position.x=o.x+Math.sin(t*.05+o.p)*8;
for(const w of W){if(w.l>0){w.l-=dt*1.8;w.s.position.addScaledVector(w.v,dt);w.s.material.opacity=Math.max(0,w.l)*.22;w.s.scale.setScalar(.6+(1-w.l)*.5)}}
cam.position.x+=(mx*1.5-cam.position.x)*.03;cam.position.y+=(7+my*.6+Math.sin(t*.3)*.3-cam.position.y)*.03;cam.position.z+=((window.CZ||34)-cam.position.z)*.05;cam.lookAt(0,9,0);R.render(sc,cam)};tick();
}catch(e){console.warn('Background scene unavailable',e);const c=$('sc');if(c)c.style.display='none'}})();
</script></body></html>
