# Snippets
#Noised Glass Morphism
```html
<div class="box">
  <div class="overlay"></div>
</div>
 


<svg width="0" height="0">
  <filter id="noise" x="0" y="0" width="100%" height="100%">
    <feTurbulence baseFrequency="0.65" numOctaves="3" type='fractalNoise' stitchTiles='stitch'/>
  </filter>
</svg>
```
```css
body{
  height:100vh;
  background:url("https://images.pexels.com/photos/33041/antelope-canyon-lower-canyon-arizona.jpg?cs=tinysrgb&w=1260&h=750&dpr=1") 
}
.box{
  height:150px;
  width:250px;
  backdrop-filter: blur(5px);
  background:rgba(255, 255, 255, 0.2);
  box-shadow: 0 4px 32px rgba(0, 0, 0, .2);
  
  position:relative;
  border-radius:1rem;
  border: 1.5px solid red;
    border-image-source: linear-gradient(135deg, #ffffff 0%, rgba(255, 255, 255, 0) 100%); 
    
}
.overlay{
  position:absolute;
  height:100%;
  width:100%;
  background:Red;
  top:0;
  left:0;
 filter: url(#noise) contrast(10%) brightness(120%) opacity(0.46);  
 clip-path: inset(0 0 0 0 round 1rem)
   /* Border Radius but for svg*/
}
```
