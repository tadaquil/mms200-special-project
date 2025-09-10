# Study with Huna APP
Study with Huna is an Augmented Reality (AR) study app designed to help students study through gamified content. It makes use of AR markers to make the app function, and it is currently running as a prototype. It has 4 sections, with each section having an introduction page, learn more section, and finally, an activity area to test your knowledge. For now, it is using information from an Oral Communication reviewer for Senior High School levels, but in the future, the developer is opting to make it universal for any subject.

Link to project: http://studywithhuna.online

How It's Made:
Tech used: HTML, CSS, JavaScript, A-Frame (three.js), AR.js, aframe-extras.loaders, Hostinger

Architecture
* Multi-page, static: one HTML per part.
* Scene & tracking: Each page mounts an <a-scene arjs embedded> and a single <a-marker type="pattern" url="...patt">.

Markers Used:
* Introductions: models/marker/huna-marker1.patt (S1 / index.html), huna-marker2.patt (S2 / s2-introduction.html), huna-marker3.patt (S3 / s3-introduction.html), huna-marker4.patt (S4 / s4-introduction.html).
* Activities & Learn More: models/marker/s{N}-activity.patt, models/marker/s{N}-learnmore.patt
