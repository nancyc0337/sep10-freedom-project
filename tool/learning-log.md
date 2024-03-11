# Tool Learning Log

Tool: **Aframe**

---

2/26/2024:
* Getting Started
  * [Youtube](https://youtu.be/jhEfT9YjLcU?si=7MmcYtvEusZUHGti) + [Replit](Replit.com) + [Aframe.io](aframe.io)
  * Watched 5-7 minutes of this video: [Easily code a virtual reality web experience with A-Frame (WebVR)](https://youtu.be/jhEfT9YjLcU?si=7MmcYtvEusZUHGti)

Link to my Tinkering: [Click Here to See My Tinkering](https://replit.com/@nancyc85/tinker#index.html)

* Created 3D shapes, change positions and color
  * How do I change the positions?

Answer: "Let’s first go over 3D space. A-Frame uses a right-handed coordinate system. With the default camera direction: positive X-axis extends right, positive Y-axis extends up, and the positive Z-axis extends out of the screen towards us:"

![Alt text](image.png)

[Aframe.io](aframe.io) shows a section of primitives. There is a lot more 3D shapes that I can use.

Starter code:
```html
<html>
  <head>
    <script src="https://cdn.jsdelivr.net/gh/aframevr/aframe@9b8609bd84a292ef97bf1e8589401ae0d3201280/dist/aframe-master.min.js"></script>
  </head>
  <body>
    <a-scene>
      <!-- ... -->
    </a-scene>
  </body>
</html>
```
 * Next Steps:
   * Finish watch the [video](https://youtu.be/jhEfT9YjLcU?si=7MmcYtvEusZUHGti)
   * Tinkering with more 3D shapes and learn to background, rotation, scale, etc.

3/10/2024:
* Finishing the [video](https://youtu.be/jhEfT9YjLcU?si=7MmcYtvEusZUHGti)
* I tinkered in [cs50.dev](cs50.dev).

Code:
```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/aframe/0.5.0/aframe.js"></script>

<a-scene>
    <a-sphere></a-sphere>
    <a-plane width="10" height="10" position="0 0 -2.5" color="black"></a-plane>
</a-scene>

<script src="index.js"></script>

$ = (queryString) => document.querySelector(queryString);

const shiftHue = (hue) => (hue + 1) % 360;

let hue = 0;

const animate = () => {
  hue = shiftHue(hue);
  const color = `hsl(${hue}, 100%, 50%)`;
  $('a-sphere').setAttribute('color', color);

  const variation = Math.sin(Date.now() / 1000);

  const position = `0 ${1.5 + variation} -2`;
  $('a-sphere').setAttribute('position', position);

  $('a-plane').setAttribute('rotation', `-90 ${90 * variation} 0`);
  $('a-plane').setAttribute('color', color);

  requestAnimationFrame(animate);
};

requestAnimationFrame(animate);
```

* Next Steps:
  * Learn the component camera [Link](https://aframe.io/docs/1.5.0/components/camera.html)

X/X/X:
* Text

X/X/X:
* Text

X/X/X:
* Text

X/X/X:
* Text

<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
