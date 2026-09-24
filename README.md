# Son-of-thunder-
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<meta name="theme-color" content="#04204a">
<title>JAKE — SONS OF THUNDER ⚡</title>

<style>
:root{
  --c:#00aaff;
  --bg:#04204a;
  --w:#fff;
  --s:#c3cddb;
  --gold:#ffd23f;
}

*{
  box-sizing:border-box;
  -webkit-tap-highlight-color:transparent;
}

html,body{
  margin:0;
  min-height:100%;
  background:var(--bg);
  color:var(--w);
}

body{
  min-height:100vh;
  font-family:"Trebuchet MS",Arial,sans-serif;
  overflow-x:hidden;
  background:
    radial-gradient(
      circle at 50% 0%,
      color-mix(in srgb,var(--c) 45%,transparent),
      transparent 55%
    ),
    linear-gradient(
      180deg,
      var(--bg),
      color-mix(in srgb,var(--bg) 55%,#000)
    );
  background-attachment:fixed;
  transition:background .5s;
}

body.t-opening,
body.t-sons{
  --bg:#04204a;
  --c:#00aaff;
}

body.t-ride{
  --bg:#4a2205;
  --c:#ff8a1f;
}

body.t-fearless{
  --bg:#5c0d0a;
  --c:#ff3b24;
}

body.t-dream{
  --bg:#2f1a70;
  --c:#b28cff;
}

body.t-daughter{
  --bg:#5a1450;
  --c:#ff6fd0;
}

body.t-mechanic{
  --bg:#222a33;
  --c:#ffb020;
}

body.t-camp{
  --bg:#0b4127;
  --c:#3ddc84;
}

body.t-prayer{
  --bg:#0a3a48;
  --c:#5ee6e0;
}

body.t-future{
  --bg:#523d05;
  --c:#ffd23f;
}

body.t-rev{
  --bg:#1a0b36;
  --c:#a855ff;
}

body.t-race{
  --bg:#08260f;
  --c:#2bff5a;
}

body.t-final{
  --bg:#04204a;
  --c:#00aaff;
}

.screen{
  display:none;
  min-height:100vh;
  padding:
    calc(20px + env(safe-area-inset-top))
    18px
    calc(80px + env(safe-area-inset-bottom));
  flex-direction:column;
}

.screen.active{
  display:flex;
  animation:screenIn .4s ease both;
}

@keyframes screenIn{
  from{
    opacity:0;
    transform:translateY(18px);
  }
  to{
    opacity:1;
    transform:none;
  }
}

.wrap{
  width:100%;
  max-width:820px;
  margin:0 auto;
}

.center{
  align-items:center;
  justify-content:center;
  text-align:center;
}

button{
  font:inherit;
  color:#fff;
  cursor:pointer;
  touch-action:manipulation;
}

.btn{
  display:inline-block;
  padding:16px 26px;
  border-radius:12px;
  border:2px solid var(--c);
  background:
    linear-gradient(
      135deg,
      color-mix(in srgb,var(--c) 40%,#000),
      rgba(0,0,0,.5)
    );
  font-weight:900;
  letter-spacing:1px;
  font-size:17px;
  min-height:54px;
  transition:
    transform .15s,
    background .15s,
    box-shadow .15s;
  box-shadow:0 0 15px color-mix(in srgb,var(--c) 35%,transparent);
}

.btn:hover{
  background:
    linear-gradient(
      135deg,
      color-mix(in srgb,var(--c) 60%,#000),
      rgba(0,0,0,.4)
    );
}

.btn:active{
  transform:scale(.96);
}

.next{
  width:100%;
  margin-top:28px;
  padding:18px 20px;
  font-size:18px;
  border-radius:14px;
  border:2px solid var(--c);
  background:
    linear-gradient(
      135deg,
      color-mix(in srgb,var(--c) 45%,#000),
      rgba(0,0,0,.55)
    );
  font-weight:900;
  box-shadow:
    0 0 18px color-mix(in srgb,var(--c) 35%,transparent);
}

.next:active{
  transform:scale(.97);
}

.brand{
  font-size:clamp(70px,22vw,130px);
  font-weight:900;
  letter-spacing:-4px;
  line-height:.9;
  text-shadow:
    0 0 10px #fff,
    0 0 30px var(--c),
    0 0 60px var(--c);
}

.sub{
  margin-top:12px;
  font-size:clamp(20px,6vw,32px);
  letter-spacing:6px;
  font-weight:800;
  color:var(--s);
}

.bolt{
  font-size:70px;
  filter:drop-shadow(0 0 18px var(--c));
  animation:pul 2s infinite;
}

@keyframes pul{
  50%{
    transform:scale(1.1);
  }
}

.race-title{
  margin:26px 0 14px;
  font-size:clamp(24px,7vw,40px);
  font-weight:900;
  text-shadow:0 0 18px var(--c);
}

.copy{
  max-width:600px;
  margin:0 auto 26px;
  line-height:1.8;
  color:var(--s);
  font-size:17px;
}

h1.t{
  margin:0 0 6px;
  font-size:clamp(38px,11vw,68px);
  line-height:1;
  font-weight:900;
  text-shadow:0 0 25px var(--c);
}

.intro{
  color:var(--s);
  font-size:18px;
  line-height:1.8;
  margin:12px 0 24px;
}

.grid{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:12px;
}

.card{
  padding:20px;
  border-radius:14px;
  border:1px solid var(--c);
  background:rgba(0,0,0,.35);
  margin:12px 0;
}

.card h3{
  margin:0 0 8px;
  color:var(--c);
  font-size:20px;
}

.card p{
  margin:0;
  line-height:1.7;
  color:var(--s);
}

.quote{
  margin:24px 0;
  padding:22px;
  border-left:5px solid var(--c);
  background:rgba(0,0,0,.3);
  font-size:clamp(22px,5.5vw,32px);
  font-weight:900;
  font-style:italic;
  line-height:1.35;
}

.big{
  margin:34px 0 10px;
  text-align:center;
  font-size:clamp(28px,8vw,52px);
  font-weight:900;
  text-shadow:0 0 25px var(--c);
}

.big-num{
  font-size:clamp(70px,24vw,140px);
  font-weight:900;
  line-height:1;
  text-shadow:0 0 30px var(--c);
}

.note{
  text-align:center;
  color:var(--s);
  font-size:12px;
  margin-top:26px;
  line-height:1.6;
}

/* JOURNEY PROGRESS */

#journeyBar{
  position:fixed;
  top:0;
  left:0;
  right:0;
  height:5px;
  z-index:200;
  background:rgba(0,0,0,.45);
}

#journeyFill{
  height:100%;
  width:0;
  background:linear-gradient(
    90deg,
    #00aaff,
    #fff,
    var(--c)
  );
  box-shadow:0 0 14px var(--c);
  transition:width .45s ease;
}

#journeyInfo{
  position:fixed;
  top:9px;
  left:50%;
  transform:translateX(-50%);
  z-index:190;
  padding:5px 11px;
  border-radius:20px;
  background:rgba(0,0,0,.55);
  border:1px solid color-mix(in srgb,var(--c) 55%,transparent);
  color:var(--s);
  font-size:10px;
  font-weight:900;
  letter-spacing:1px;
  white-space:nowrap;
}

/* MILESTONE */

.milestone{
  position:fixed;
  left:50%;
  top:50%;
  transform:translate(-50%,-50%) scale(.7);
  z-index:500;
  width:min(88vw,440px);
  padding:30px 22px;
  text-align:center;
  border:2px solid var(--c);
  border-radius:20px;
  background:
    radial-gradient(
      circle at center,
      color-mix(in srgb,var(--c) 30%,#000),
      #050505 75%
    );
  box-shadow:
    0 0 40px var(--c),
    0 0 100px color-mix(in srgb,var(--c) 45%,transparent);
  opacity:0;
  pointer-events:none;
}

.milestone.show{
  animation:milestoneShow 2.1s ease both;
}

.milestone-icon{
  font-size:55px;
}

.milestone-small{
  margin-top:8px;
  color:var(--s);
  font-size:12px;
  letter-spacing:3px;
  font-weight:900;
}

.milestone-title{
  margin-top:8px;
  font-size:30px;
  font-weight:900;
  text-shadow:0 0 18px var(--c);
}

@keyframes milestoneShow{
  0%{
    opacity:0;
    transform:translate(-50%,-50%) scale(.7);
  }
  15%{
    opacity:1;
    transform:translate(-50%,-50%) scale(1.03);
  }
  25%{
    transform:translate(-50%,-50%) scale(1);
  }
  80%{
    opacity:1;
  }
  100%{
    opacity:0;
    transform:translate(-50%,-50%) scale(.95);
  }
}

/* FLASH */

.flash{
  position:fixed;
  inset:0;
  background:#fff;
  opacity:0;
  pointer-events:none;
  z-index:450;
}

.flash.go{
  animation:fl .25s;
}

@keyframes fl{
  0%{opacity:.35}
  100%{opacity:0}
}

/* LIGHTNING */

.zap{
  position:fixed;
  pointer-events:none;
  z-index:460;
  font-size:44px;
  transform:translate(-50%,-50%);
  animation:zap .6s ease-out forwards;
  filter:drop-shadow(0 0 12px #fff);
}

@keyframes zap{
  to{
    opacity:0;
    transform:translate(-50%,-90%) scale(1.8);
  }
}

/* PHOTO */

.pic{
  min-height:240px;
  margin:20px 0;
  border:2px dashed var(--c);
  border-radius:16px;
  display:flex;
  flex-direction:column;
  align-items:center;
  justify-content:center;
  text-align:center;
  padding:16px;
  background:rgba(0,0,0,.25);
  overflow:hidden;
}

.pic img{
  max-width:100%;
  max-height:420px;
  border-radius:12px;
}

/* METER */

.meter{
  height:22px;
  border-radius:12px;
  background:rgba(0,0,0,.5);
  border:2px solid var(--c);
  overflow:hidden;
  margin:16px 0;
}

.meter i{
  display:block;
  height:100%;
  width:0;
  background:linear-gradient(
    90deg,
    #3ddc84,
    #ffd23f,
    #ff2d4d
  );
}

/* RACE LIGHTS */

.lights{
  display:flex;
  gap:
