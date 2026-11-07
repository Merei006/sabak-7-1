<!DOCTYPE html>
<html lang="kk"><head><meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Ақпараттың өлшем бірлігі — 1-сабақ, практикалық жұмыс</title>
<style>
:root{--bg:#f6f4ee;--card:#ffffff;--ink:#1d2433;--navy:#14213d;--acc:#f4a261;--ok:#1f7a4d;--bad:#b3261e;--line:#d9d6cc;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#10151f;--card:#1b2333;--ink:#e8ebf2;--navy:#f4a261;--line:#33405a;--ok:#5fd39a;--bad:#ff8a80}}
html{scroll-padding-top:env(safe-area-inset-top,0px)}
*{box-sizing:border-box}
body{margin:0;background:var(--bg);color:var(--ink);font-family:system-ui,-apple-system,"Segoe UI",Arial,sans-serif;line-height:1.45}
main{max-width:820px;margin:0 auto;padding:20px 16px 48px}
h1{font-size:1.5rem;color:var(--navy);margin:0 0 4px}
.sub{margin:0 0 16px;opacity:.8}
nav{display:flex;gap:8px;margin-bottom:16px}
nav button{flex:1;padding:12px;border:2px solid var(--navy);background:var(--card);color:var(--ink);border-radius:10px;font-size:1rem;cursor:pointer}
nav button.on{background:var(--navy);color:var(--bg);font-weight:700}
.lv{margin:20px 0 8px;color:var(--navy);font-size:1.15rem}
.t{background:var(--card);border:1px solid var(--line);border-radius:12px;padding:14px;margin-bottom:10px}
.t p{margin:0 0 8px}
.r{display:flex;gap:8px;align-items:center;flex-wrap:wrap}
input,select{font-size:1rem;padding:8px 10px;border:1px solid var(--line);border-radius:8px;background:var(--bg);color:var(--ink);min-width:120px}
button.chk{padding:8px 14px;border:0;border-radius:8px;background:var(--acc);color:#14213d;font-weight:700;cursor:pointer;font-size:1rem}
.m{font-weight:700}.ok{color:var(--ok)}.bad{color:var(--bad)}
.hint{font-size:.9rem;opacity:.8;margin-top:6px}
.score{position:sticky;bottom:0;background:var(--navy);color:var(--bg);padding:12px 16px;border-radius:12px;margin-top:20px;font-weight:700;text-align:center}
.reset{margin-top:8px;padding:8px 14px;border:1px solid var(--navy);background:transparent;color:var(--ink);border-radius:8px;cursor:pointer;font-size:1rem}
.rule{background:var(--card);border-left:6px solid var(--acc);padding:10px 14px;border-radius:8px;margin-bottom:12px}
</style></head><body><main>
<h1>Ақпараттың өлшем бірлігі</h1>
<p class="sub">7-сынып · Информатика · 1-сабақ · Практикалық жұмыс (оқу мақсаты 7.2.1.1)</p>

<div id="app"></div>
</main>
<script>
var D={l1:{"rule": "1 байт = 8 бит. Әр келесі бірлік алдыңғысынан 1024 есе үлкен: байт → Кбайт → Мбайт → Гбайт → Тбайт. Үлкеннен кішіге — × 1024, кішіден үлкенге — ÷ 1024.", "secs": [{"t": "Бірліктерді сәйкестендір", "items": [{"q": "Ақпараттың ең кіші бірлігі", "type": "sel", "opts": ["бит", "байт", "Кбайт"], "a": "бит"}, {"q": "1 байт =", "type": "sel", "opts": ["8 бит", "10 бит", "1024 бит"], "a": "8 бит"}, {"q": "1 Кбайт =", "type": "sel", "opts": ["1000 байт", "1024 байт", "8 байт"], "a": "1024 байт"}, {"q": "1 Мбайт =", "type": "sel", "opts": ["1024 Кбайт", "1024 байт", "1024 Гбайт"], "a": "1024 Кбайт"}, {"q": "1 Гбайт =", "type": "sel", "opts": ["1024 Кбайт", "1024 Тбайт", "1024 Мбайт"], "a": "1024 Мбайт"}, {"q": "1 Тбайт =", "type": "sel", "opts": ["1024 Мбайт", "1024 Гбайт", "1024 Пбайт"], "a": "1024 Гбайт"}]}, {"t": "Сәйкестендір: бірлік және оның мәні", "pairs": [["1 байт", "8 бит"], ["1 Кбайт", "1024 байт"], ["1 Мбайт", "1024 Кбайт"], ["1 Гбайт", "1024 Мбайт"], ["1 Тбайт", "1024 Гбайт"]]}, {"t": "Дұрыс па, бұрыс па?", "items": [{"q": "Бит — ақпараттың ең кіші бірлігі", "type": "sel", "opts": ["Дұрыс", "Бұрыс"], "a": "Дұрыс"}, {"q": "1 Кбайт = 1000 байт", "type": "sel", "opts": ["Дұрыс", "Бұрыс"], "a": "Бұрыс", "h": "1 Кбайт = 1024 байт"}, {"q": "Гбайт Мбайттан үлкен", "type": "sel", "opts": ["Дұрыс", "Бұрыс"], "a": "Дұрыс"}, {"q": "1 байт бір символды кодтайды", "type": "sel", "opts": ["Дұрыс", "Бұрыс"], "a": "Дұрыс"}, {"q": "Тбайт Гбайттан кіші", "type": "sel", "opts": ["Дұрыс", "Бұрыс"], "a": "Бұрыс", "h": "Тбайт Гбайттан 1024 есе үлкен"}]}, {"t": "Өсу ретімен орналастыр", "items": [{"q": "а) Гбайт  ә) Кбайт  б) Тбайт  в) Мбайт. Әріптерді қатар жаз", "a": "әваб", "h": "кішіден үлкенге: Кбайт, Мбайт, Гбайт, Тбайт"}, {"q": "а) Мбайт  ә) байт  б) Гбайт  в) Кбайт. Әріптерді қатар жаз", "a": "әваб", "h": "байт, Кбайт, Мбайт, Гбайт"}]}, {"t": "Үлкеннен кішіге (× 1024)", "items": [{"q": "1 Кбайт = ? байт", "a": "1024"}, {"q": "2 Кбайт = ? байт", "a": "2048", "h": "2 × 1024"}, {"q": "4 Мбайт = ? Кбайт", "a": "4096", "h": "4 × 1024"}, {"q": "3 Гбайт = ? Мбайт", "a": "3072", "h": "3 × 1024"}, {"q": "2 Тбайт = ? Гбайт", "a": "2048", "h": "2 × 1024"}, {"q": "Қатені түзет: оқушы 2 Кбайт = 2000 байт деп жазды. Дұрыс жауабы қанша байт?", "a": "2048", "h": "1 Кбайт = 1024 байт"}]}, {"t": "Сәйкестендір: көлем және оның мәні", "pairs": [["2 Кбайт", "2048 байт"], ["3 Мбайт", "3072 Кбайт"], ["4 Гбайт", "4096 Мбайт"], ["5 Кбайт", "5120 байт"], ["1 Тбайт", "1024 Гбайт"]]}, {"t": "Кішіден үлкенге (÷ 1024)", "items": [{"q": "3072 байт = ? Кбайт", "a": "3", "h": "3072 ÷ 1024"}, {"q": "8192 Кбайт = ? Мбайт", "a": "8", "h": "8192 ÷ 1024"}, {"q": "10240 Мбайт = ? Гбайт", "a": "10", "h": "10240 ÷ 1024"}, {"q": "4096 Гбайт = ? Тбайт", "a": "4", "h": "4096 ÷ 1024"}]}, {"t": "Сәйкестендір: түрлендіру және амал", "pairs": [["Кбайт → байт", "× 1024"], ["Гбайт → Мбайт", "× 1024"], ["байт → Кбайт", "÷ 1024"], ["Мбайт → Гбайт", "÷ 1024"]]}, {"t": "Екі қадамды түрлендіру", "items": [{"q": "2 Мбайт = ? байт", "a": "2097152", "h": "алдымен Кбайтқа (× 1024), сосын байтқа (× 1024)"}, {"q": "5 Мбайт = ? байт", "a": "5242880", "h": "5 × 1024 × 1024"}, {"q": "3 Гбайт = ? Кбайт", "a": "3145728", "h": "3 × 1024 × 1024"}, {"q": "1 048 576 байт = ? Мбайт", "a": "1", "h": "екі рет ÷ 1024"}]}, {"t": "Сақтау құрылғылары", "items": [{"q": "Флеш-жад 16 Гбайт = ? Мбайт", "a": "16384", "h": "16 × 1024"}, {"q": "Сыртқы диск 2 Тбайт = ? Гбайт", "a": "2048", "h": "2 × 1024"}, {"q": "CD-дағы файл 3072 Кбайт = ? Мбайт", "a": "3", "h": "3072 ÷ 1024"}, {"q": "1 Гбайт флешке көлемі 100 Мбайт неше файл сияды?", "a": "10", "h": "1 Гбайт ≈ 1000 Мбайт деп емес, 1024 ÷ 100 = 10,24 — толық саны"}]}, {"t": "Сәйкестендір: құрылғы және көлемі", "pairs": [["CD", "≈ 700 Мбайт"], ["DVD", "≈ 4,7 Гбайт"], ["Флеш-жад", "8–64 Гбайт"], ["Сыртқы диск", "500 Гбайт және одан жоғары"]]}, {"t": "Сәйкестендір: ақпарат бірлігі және мағынасы", "pairs": [["Бит", "0 немесе 1"], ["Байт", "бір символ (8 бит)"], ["Кбайт", "1024 байт"], ["Гбайт", "1024 Мбайт"]]}]}};
var cur="l1",ok=0,tot=0,done={};
var sc;
function upd(){sc.textContent="Нәтиже: "+ok+" / "+tot}
function shuf(a){a=a.slice();for(var i=a.length-1;i>0;i--){var j=Math.floor(Math.random()*(i+1));var t=a[i];a[i]=a[j];a[j]=t}return a}
function renderMatch(s,si,app){
 var rights=shuf(s.pairs.map(function(p){return p[1]}).filter(function(v,i,a){return a.indexOf(v)==i}));
 var box=el("div","t"),sels=[],ms=[];
 s.pairs.forEach(function(p,i){tot++;
  var r=el("div","r");r.style.marginBottom="8px";
  var l=el("span","",p[0]);l.style.flex="1";l.style.minWidth="140px";
  var f=el("select");var o0=el("option","","— таңда —");o0.value="";f.appendChild(o0);
  rights.forEach(function(x){var op=el("option","",x);op.value=x;f.appendChild(op)});
  var m=el("span","m");r.appendChild(l);r.appendChild(f);r.appendChild(m);box.appendChild(r);sels.push(f);ms.push(m)});
 var b=el("button","chk","Тексер");
 b.onclick=function(){s.pairs.forEach(function(p,i){var v=sels[i].value;if(!v)return;var good=v==p[1],id=si+"_"+i;if(good&&!done[id]){done[id]=true;ok++}ms[i].className="m "+(good?"ok":"bad");ms[i].textContent=good?"✓":"✗"});upd()};
 box.appendChild(b);app.appendChild(box)}
function norm(s){return String(s).replace(/[\s\u00a0]/g,"").replace(",",".").toLowerCase()}
function el(tag,cls,txt){var e=document.createElement(tag);if(cls)e.className=cls;if(txt!==undefined)e.textContent=txt;return e}
function show(k){
 cur=k;ok=0;tot=0;done={};
 
 
 
 var app=document.getElementById("app");app.innerHTML="";
 var d=D[k];app.appendChild(el("div","rule",d.rule));
 sc=el("div","score","Нәтиже: 0 / 0");
 d.secs.forEach(function(s,si){
  app.appendChild(el("h2","lv",(si+1)+"-тапсырма. "+s.t));
  if(s.pairs){renderMatch(s,si,app);return}
  s.items.forEach(function(it,ii){
   var id=si+"_"+ii;tot++;
   var box=el("div","t");box.appendChild(el("p","",it.q));
   var r=el("div","r"),f;
   if(it.type=="sel"){f=el("select");var o0=el("option","","— таңда —");o0.value="";f.appendChild(o0);it.opts.forEach(function(o){var op=el("option","",o);op.value=o;f.appendChild(op)})}
   else{f=el("input");f.type="text";f.inputMode="text";f.placeholder="жауабың"}
   var b=el("button","chk","Тексер"),m=el("span","m");
   b.onclick=function(){
    if(!norm(f.value))return;
    var good=norm(f.value)==norm(it.a);
    if(!(id in done)){done[id]=good;if(good)ok++}
    else if(good&&!done[id]){done[id]=true;ok++}
    m.className="m "+(good?"ok":"bad");
    m.textContent=good?"✓ Дұрыс!":"✗ Қайта көр";
    sc.textContent="Нәтиже: "+ok+" / "+tot;
    hint.style.display=good?"none":"block"};
   r.appendChild(f);r.appendChild(b);r.appendChild(m);box.appendChild(r);
   var hint=el("div","hint",it.h?"Кеңес: "+it.h:"");hint.style.display="none";box.appendChild(hint);
   app.appendChild(box)})});
 upd();app.appendChild(sc);
 var rb=el("button","reset","Қайта бастау");rb.onclick=function(){show(cur)};app.appendChild(rb)}
show("l1");
</script></body></html>
