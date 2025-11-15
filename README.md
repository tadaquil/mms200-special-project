# Study with Huna APP
Study with Huna is an Augmented Reality (AR) study app designed to help students study through gamified content. It makes use of AR markers to make the app function, and it is currently running as a prototype. It has 4 sections, with each section having an introduction page, learn more section, and finally, an activity area to test your knowledge. For now, it is using information from an Oral Communication reviewer for Senior High School levels, but in the future, the developer is opting to make it universal for any subject.

Link to project: https://iop.upou.edu.ph/ar/studywithhuna/

Link to access the reviewer for printing: https://drive.google.com/file/d/1FeMyfPPVzCpXbgmLSxZq7pEyR_cKqKQJ/view?usp=sharing

How It's Made: HTML, CSS, JavaScript, A-Frame (three.js), AR.js, aframe-extras.loaders, Hostinger

Architecture
* Multi-page, static: one HTML per part.

Markers Used
* Introductions: models/marker/huna-marker1.patt (S1 / index.html), huna-marker2.patt (S2 / s2-introduction.html), huna-marker3.patt (S3 / s3-introduction.html), huna-marker4.patt (S4 / s4-introduction.html).
* Activities: models/marker/s1-activity.patt, models/marker/s2-activity.patt, models/marker/s3-activity.patt, models/marker/s4-activity.patt,
* Learn More: models/marker/s1-learnmore.patt, models/marker/s2-learnmore.patt, models/marker/s3-learnmore.patt, models/marker/s4-learnmore.patt

Optimizations
* Preload critical UI to avoid first-tap stutter.
* Accurate colors for UI using ui-texture-correct (toneMapping off, sRGB textures).
* Marker-follow without jitter using follow-marker to stabilize the UI plane while keeping it front-facing.
* Scoped loading per page: each HTML only loads the assets it needs.

Next-step improvements
* Convert heavy PNGs to WebP/AVIF with PNG fallback.
* Draco-compress GLBs; reuse a single avatar rig across sections.
* Add a Service Worker to cache markers/UI/audio for flaky school Wi-Fi.
* Idle prefetch the next dialogue image/audio after the first gesture.
