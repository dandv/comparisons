# Star rating widgets

While building a [star rating widget for AMP](https://github.com/ampproject/amphtml/issues/2691), I've evaluated 40+ GitHub projects, codepends, Fiddles and StackOverflow samples. Here are the results, excluding projects that had no stars or issues, or have not been updated in more than two years.

Some widgets insist on using only CSS. This has academic value, but is an unrealistic requirement, and makes it impossible to get other functionality right, such as [keyboard accessibility that doesn't go backwards](https://github.com/LunarLogic/starability/issues/15).

Other widgets depend on jQuery (most often), React, Angular, or Vue. Hard to see how this is necessary, when [writing plain JavaScript modules](https://pinboard.in/u:dandv/b:0abee96871f2) is a much better idea for serveral good reasons.


## Superset of features

* Touch and mouse (pointer) friendly
* Customizable number of stars
* [Half-stars](https://codepen.io/jamesbarnett/pen/vlpkh), even [fluid/fully fractional stars](https://jsfiddle.net/craig_h_411/992o7cq5/) input
* Read-only/display a given (possibly [fractional](http://codepen.io/Bluetidepro/pen/GkpEa)) rating
* [Configurable icons](http://auxiliary.github.io/rater) instead of stars, or images/SVGs
* Clean scalable vector icons ([e.g. Font Awesome](http://www.cssscript.com/simple-5-star-rating-system-with-css-and-html-radios/)) for consistent display across devices, instead of images
* Custom styles for the icons
* Optional selection result/label (updated on hover or after click)
* Configurable tooltips and captions for each star value
* Optional [animated feedback on selection](http://lunarlogic.github.io/starability/)
* After click and the selection "sticking", mousing over it shows the new potential selection in a visually different way, and the existing selection persists until the next click/tap ([Lea Verou](http://lea.verou.me/2011/08/accessible-star-rating-widget-with-pure-css/))
* [Keyboard](https://developer.mozilla.org/en-US/docs/Web/Accessibility/An_overview_of_accessible_web_applications_and_widgets#Keyboard_navigation) accessibility: [right arrow increases the rating, left arrow decreases it](http://codepen.io/mburnette/pen/eNNZbm)
* "Clear" button
* [Right-To-Left input support](http://plugins.krajee.com/star-rating-demo-basic-usage#basic-example-8)


## CSS only implementations

- [dandv's CSS-only properly keyboard-accessible](http://jsbin.com/zejeba/) solution
- [half stars, clear, not accessible](https://codepen.io/mrk1989/pen/mLeHJ) - reverse DOM order
- [Lea Verou's radio buttons (2011)](http://lea.verou.me/2011/08/accessible-star-rating-widget-with-pure-css/) with keyboard accessibility (though buggy - perssing arrow keys goes backwards), and selected stars are offset by a few pixels in Firefox: 
![image](https://cloud.githubusercontent.com/assets/33569/22502661/b4e914f0-e822-11e6-9c05-9f9d10cd3035.png)
- https://css-tricks.com/star-ratings/ - 2012, using `unicode-bidi: bidi-override;`. Mouseover flicker.
- [radio buttons, not keyboard-accessible, but selection "sticks"](https://www.everythingfrontend.com/posts/star-rating-input-pure-css.html); - pixel shift on hover
- [half stars, stickiness, Font Awesome](https://codepen.io/jamesbarnett/pen/vlpkh); 2015
- [no reversal](http://jsfiddle.net/y9zeLr1n/26/) but not keyboard accessible, not sticky, no half stars


## Notable libraries [without dependencies](https://github.com/GiuseppeScalese/JS-Star-Rating-Widget/issues/1)

- [starability](https://github.com/LunarLogic/starability/issues/17) - uses images, [keyboard arrows work reversed](https://github.com/LunarLogic/starability/issues/15)
- [BioPhoton](https://github.com/BioPhoton/css-star-rating) - long feature list, no demo, docs need proofreading
- [SVG-based, no keyboard accessibility](https://github.com/aaronpk/rating-stars); public domain license
- [geminilabs](https://github.com/geminilabs/star-rating.js); lots of JS, [keyboard arrows still work backwards](https://github.com/geminilabs/star-rating.js/issues/1)
- [juliangruber's](https://github.com/juliangruber/rating); no real commits since 2013, no feature list; JS API


## Web components
- PolymerLabs has a [component](https://github.com/PolymerLabs/star-ratings), that depends on `iron-icon`
- [cvmartinez's component depending on Polymer's paper-icon](https://github.com/cmartinezv/star-rating)
- [Nevraeka's](https://github.com/Nevraeka/star-rating) - keyboard accessibility, custom # of stars, custom size


## For API and features reference
* [Krajee](http://plugins.krajee.com/star-rating)'s full-featured Bootstrap + jQuery star-rating plugin: SVG, customizable icons, [fractional rating](http://plugins.krajee.com/star-rating-demo-basic-usage#basic-example-2), RTL support. [Not accessible](https://github.com/kartik-v/bootstrap-star-rating/issues/129).
* [antenna.io jQuery bar rating](http://antenna.io/demo/jquery-bar-rating/examples/) - great documentation, keyboard accessible via Tab (though not arrows); display but not input fractional stars
* Auxiliary's [rater](http://auxiliary.github.io/rater/) - customizable UTF-8 characters, Font-Awesome icons, or even HTML; supports half ratings
* [awesome-rating](https://github.com/bandraszyk/awesome-rating) - customizable Font-Awesome icons
* [jQuery RateIt](http://stackoverflow.com/questions/4542883/jquery-star-rating/13176213#13176213)
* [vue-star-rating](https://github.com/craigh411/vue-star-rating) - half-star rating, fluid rating
* [SVG-based jQuery plugin](https://github.com/nashio/star-rating-svg/) with good list of features: different shapes, half stars, read-only mode, onhover and onrating callbacks/events
* [react](https://github.com/voronianski/react-star-rating-component) - 79 stars; [no color change on hover](https://github.com/voronianski/react-star-rating-component/issues/19)
* [`<input type="number">`](https://github.com/javiertoledo/bootstrap-rating-input)


## Rejected libraries
* [Adobe Spry](https://adobe.github.io/Spry/samples/rating/RatingSample.html)
* [CallMeNick's - nothing special](https://github.com/callmenick/five-star-rating/issues/9), abandoned since 2015
* [many others omitted]


## StackOverflow discussions

* [jQuery and CSS - display only](http://stackoverflow.com/questions/1987524/turn-a-number-into-star-rating-display-using-jquery-and-css?rq=1)
* [jQuery star rating plugins](http://stackoverflow.com/questions/4542883/jquery-star-rating)
