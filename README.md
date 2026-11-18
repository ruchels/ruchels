(function() {
var topLangs = (github && github.languages && github.languages.length > 0 ? github.languages.slice(0, 6).map(function(l) { return l.name; }) : \['TypeScript', 'React', 'Next.js', 'C++', 'Go', 'Rust']);
var categories = \[
{ title: 'Languages', color: '#a78bfa', items: topLangs },
{ title: 'Frameworks', color: '#60a5fa', items: \['React Native', 'React', 'Next.js'] },
];

return (

   <div style={{
     width: '100%', height: '100%',
     background: '#08080c',
     display: 'flex', flexDirection: 'column',
     fontFamily: 'Inter', padding: '18px 32px', gap: 14,
     borderRadius: 16, border: '1px solid rgba(110,80,220,0.18)',
     position: 'relative', overflow: 'hidden',
   }}>

```
 <style>
   {`
     @keyframes float-slow {
       0%, 100% { transform: translateX(0px); opacity: 0.8; }
       50% { transform: translateX(350px); opacity: 1.2; }
     }
     @keyframes float-medium {
       0%, 100% { transform: translateX(0px); opacity: 0.7; }
       50% { transform: translateX(-250px); opacity: 1.1; }
     }
     @keyframes float-fast {
       0%, 100% { transform: translateX(0px); opacity: 0.9; }
       50% { transform: translateX(200px); opacity: 0.6; }
     }
     @keyframes float-diagonal {
       0%, 100% { transform: translate(0px, 0px); opacity: 0.75; }
       50% { transform: translate(120px, 30px); opacity: 1.0; }
     }
     @keyframes float-wave {
       0%, 100% { transform: translateX(0px); opacity: 0.65; }
       33% { transform: translateX(-160px); opacity: 0.9; }
       66% { transform: translateX(80px); opacity: 1.0; }
     }
     @keyframes float-pulse {
       0%, 100% { transform: scale(1); opacity: 0.8; }
       50% { transform: scale(1.3); opacity: 0.4; }
     }
     #glow-1 { animation: float-slow 9s ease-in-out infinite; }
     #glow-2 { animation: float-medium 12s ease-in-out infinite; }
     #glow-3 { animation: float-fast 8s ease-in-out infinite; }
     #glow-4 { animation: float-diagonal 11s ease-in-out infinite reverse; }
     #glow-5 { animation: float-wave 14s ease-in-out infinite reverse; }
     #glow-6 { animation: float-pulse 6s ease-in-out infinite; }
   `}
 </style>

 <svg width="860" height="168" style={{ position: 'absolute', top: 0, left: 0 }}>
   <defs>
     <radialGradient id="g1" cx="50%" cy="50%" r="50%">
       <stop offset="0%" stopColor="rgba(115,20,215,0.68)" />
       <stop offset="42%" stopColor="rgba(85,15,175,0.30)" />
       <stop offset="70%" stopColor="rgba(85,15,175,0)" />
     </radialGradient>
     <radialGradient id="g2" cx="50%" cy="50%" r="50%">
       <stop offset="0%" stopColor="rgba(55,55,255,0.55)" />
       <stop offset="45%" stopColor="rgba(35,45,210,0.22)" />
       <stop offset="70%" stopColor="rgba(35,45,210,0)" />
     </radialGradient>
     <radialGradient id="g3" cx="50%" cy="50%" r="50%">
       <stop offset="0%" stopColor="rgba(0,130,255,0.42)" />
       <stop offset="50%" stopColor="rgba(0,100,220,0.16)" />
       <stop offset="70%" stopColor="rgba(0,100,220,0)" />
     </radialGradient>
     <radialGradient id="g4" cx="50%" cy="50%" r="50%">
       <stop offset="0%" stopColor="rgba(0,185,240,0.32)" />
       <stop offset="70%" stopColor="rgba(0,185,240,0)" />
     </radialGradient>
     <radialGradient id="g5" cx="50%" cy="50%" r="50%">
       <stop offset="0%" stopColor="rgba(100,25,205,0.42)" />
       <stop offset="70%" stopColor="rgba(100,25,205,0)" />
     </radialGradient>
     <radialGradient id="g6" cx="50%" cy="50%" r="50%">
       <stop offset="0%" stopColor="rgba(60,80,255,0.35)" />
       <stop offset="70%" stopColor="rgba(60,80,255,0)" />
     </radialGradient>
   </defs>
   <ellipse id="glow-1" cx="170" cy="168" rx="260" ry="170" fill="url(#g1)" />
   <ellipse id="glow-2" cx="320" cy="178" rx="220" ry="140" fill="url(#g2)" />
   <ellipse id="glow-3" cx="460" cy="178" rx="190" ry="130" fill="url(#g3)" />
   <ellipse id="glow-4" cx="590" cy="188" rx="160" ry="110" fill="url(#g4)" />
   <ellipse id="glow-5" cx="750" cy="188" rx="140" ry="100" fill="url(#g5)" />
   <ellipse id="glow-6" cx="420" cy="138" rx="100" ry="80" fill="url(#g6)" />
 </svg>

 <div style={{ display:'flex', fontSize:10, fontWeight:700, color:'rgba(155,140,210,0.5)', letterSpacing:'3px' }}>
   TECH STACK
 </div>
 <div style={{ display:'flex', flexDirection:'column', gap:14 }}>
   {categories.map(function(cat) {
     return (
       <div key={cat.title} style={{ display:'flex', alignItems:'center', gap:16 }}>
         <div style={{ display:'flex', fontSize:10, fontWeight:700, color:cat.color, letterSpacing:'1px', width:80 }}>
           {cat.title.toUpperCase()}
         </div>
         <div style={{ display:'flex', flexWrap:'wrap', gap:7 }}>
           {cat.items.map(function(item) {
             return (
               <div key={item} style={{
                 display:'flex', padding:'4px 13px', borderRadius:6,
                 background:cat.color + '15', border:'1px solid ' + cat.color + '35',
                 color:'rgba(225,220,255,0.85)', fontSize:12, fontWeight:600,
               }}>{item}</div>
             );
           })}
         </div>
       </div>
     );
   })}
 </div>
```

   </div>
 );
})()
