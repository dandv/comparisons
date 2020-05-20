---


---

<h1 id="javascript-error-monitoring-services">JavaScript error monitoring services</h1>
<p>A collection of JavaScript error logging services and their description, greatly expanded from the original hosted <a href="https://github.com/cheeaun/javascript-error-logging/blob/master/README.md">here</a>.</p>
<p>Sorted descending (roughly) by feature set. Unique features are <strong>highlighted</strong>.</p>
<h2 id="glossary--features-to-look-for">Glossary / features to look for</h2>
<ul>
<li>APM - Application Performance Monitoring (<a href="https://raygun.com/platform/apm">example</a>)</li>
<li>breadcrumbs - attach a trail of the events through your system leading up to the moment a crash report was generated (<a href="https://raygun.com/documentation/language-guides/javascript/crash-reporting/breadcrumbs/">example</a>)</li>
<li>error grouping - group together errors originating from the same line (essential and common feature, offered by the vast majority of services)</li>
<li>RUM - Real User Monitoring (<a href="https://raygun.com/platform/real-user-monitoring">example</a>)</li>
<li>session replay - see exactly what the user saw in their browser (<a href="https://logrocket.com/">example</a>)</li>
<li>source maps - map your obfuscated production code back to the original source</li>
<li>stack traces - essential feature</li>
</ul>
<h2 id="hosted-services">Hosted services</h2>
<ul>
<li><a href="https://raygun.com/">Raygun</a> - Error and crash reporting software, stack traces, breadcrumbs, source map support, custom data and tags, filtering, email and chat alerts, sensitive data filtering, deployment tracking, user tracking (retrace URL navigation) and <a href="https://raygun.com/platform/real-user-monitoring">real user monitoring (RUM)</a>. Works with every major language and platform (frontend, backend and mobile).</li>
<li><a href="https://logrocket.com/">Log Rocket</a> - “pixel-perfect” <strong>session replay</strong>, network activity, console logs, surfacing user frustration (“rage click”); SDKs for Vue, React, Redux, Angular, Ember; integrations with JIRA, GitHub, Sentry, Rollbar, Segment, Trello etc. Run on-premise (ask sales for demo) or in the cloud. No server-side (Node.js) support.</li>
<li><a href="https://bugsnag.com/">Bugsnag</a> - <a href="https://www.bugsnag.com/platforms/node-js">Node.js</a> and <a href="https://docs.bugsnag.com/platforms/javascript/">client-side JS</a> (React, Vue, Angular, Ember] plus Android &amp; iOS; alerting integrations (Slack, email etc.); stability score; <a href="https://www.bugsnag.com/product"><strong>retrace user actions</strong> / automatic breadcrumbs</a> (“automatically captures a timeline of actions and events, like button presses and database queries, leading up to the error”); numerous <a href="https://www.bugsnag.com/integrations">integrations</a></li>
<li><a href="https://www.catchjs.com">CatchJS</a> - Screenshots, click trails, email notifications, remote object logging, intelligent error grouping. Extremely lightweight, only 1.78KB.</li>
<li><a href="http://errorception.com/">Errorception</a> - translate error messages to English; stack traces, source maps, smart grouping</li>
<li><a href="https://www.airbrake.io/">Airbrake</a> - tracekit, source maps. <a href="https://github.com/airbrake/airbrake-js/issues/82">No automatic error capture</a>.</li>
<li><a href="https://therootcause.io/">The Root Cause</a> - RootCause provides you with a comprehensive set of tools to monitor and reproduce errors in web sites / applications. Using the built-in recorder feature you’ll know exactly what the user did. By Bryntum who also makes <a href="https://www.bryntum.com/products/siesta/">Siesta</a> js ui + unit testing tool</li>
<li><a href="https://www.sentry.io/">Sentry</a> - source maps, tracekit, breadcrumbs, <a href="https://blog.sentry.io/2016/08/10/react-minified-errors.html">inline React error codes</a>; <a href="https://sentry.io/pricing">free for &lt;10,000 events/month</a>; open source <a href="https://github.com/getsentry/sentry">server</a> and <a href="https://github.com/getsentry/raven-js">clients</a></li>
<li><a href="https://rollbar.com/">Rollbar</a> - can <a href="https://github.com/rollbar/rollbar.js/issues/108#issuecomment-121448333">trace errors in 3rd party scripts</a> as well; <a href="https://rollbar.com/pricing/">free for &lt;5000 events/month</a>; source maps</li>
<li><a href="http://trackjs.com/">TrackJS</a> - stores timeline of events that have lead to the error</li>
<li><a href="http://usersnap.com/">Usersnap</a> - stack traces; <a href="https://usersnap.com/features/console-recorder">console recorder include XHR monitoring</a></li>
<li><a href="https://www.atatus.com/">Atatus</a> - real user monitoring (RUM), source maps, tracekit, timeline of events</li>
<li><a href="https://www.loggly.com/docs/javascript/">Loggly</a> - <a href="https://github.com/loggly/loggly-jslogger/issues/24">no stack tracing</a></li>
<li><a href="https://ruxit.com/web-monitoring/">Ruxit Web Monitoring</a> - real user and synthetic monitoring including stacktraces, originating user action and detailed browser metrics.</li>
<li><a href="https://newrelic.com/products/browser-monitoring">NewRelic Browser</a> - JS errors, real user monitoring, AJAX request insights</li>
<li><a href="http://www.muscula.com/">Muscula</a> - lor and optionally alert about client-side JS errors. Source map support. No other major features.</li>
<li><a href="http://jserrlog.appspot.com/">jsErrLog</a> - running on the free Google AppEngine</li>
<li><a href="https://www.honeybadger.io/">Honeybadger</a></li>
<li><a href="http://www.errorstack.com/">ErrorStack</a></li>
<li><a href="http://jslogger.com/">JSLogger</a></li>
<li><a href="https://appsignal.com/javascript/">AppSignal</a></li>
</ul>
<h2 id="self-hosted-services">Self-hosted services</h2>
<ul>
<li><a href="http://jsnlog.com/">JSNLog</a></li>
</ul>
<h2 id="comparisons-between-services">Comparisons between services</h2>
<ul>
<li><a href="http://www.slant.co/topics/2615/~what-are-the-best-javascript-client-side-error-logging-services">Slant on JavaScript client-side error logging services</a></li>
<li><a href="https://docs.google.com/spreadsheets/d/1IAurU073WiEr8hLeRu6rU_ilX-gaSOXfluXjUlTcQhc/edit#gid=0">Comparison matrix in a Google Sheet</a> by Igor Santos</li>
</ul>
<h2 id="dead-services">Dead services</h2>
<ul>
<li><a href="https://www.exceptionsjs.com/">https://www.exceptionsjs.com/</a></li>
<li><a href="https://getcoalmine.com/">https://getcoalmine.com/</a> [DEAD, Nov 8, 2013]</li>
<li><a href="http://damnit.jupiterit.com/">http://damnit.jupiterit.com/</a> [DEAD]</li>
<li><a href="http://rescuejs.com/">http://rescuejs.com/</a> [DEAD, acquired by Bugsnag]</li>
<li><a href="https://errplane.com/">https://errplane.com/</a> [DEAD, pivoted]</li>
<li><a href="http://jserror.net/">http://jserror.net/</a> [DEAD, probably]</li>
<li><a href="http://www.errorify.com/">http://www.errorify.com/</a> - source maps [DEAD]</li>
<li><a href="https://www.proxino.com/">https://www.proxino.com/</a> [DEAD]</li>
<li><a href="http://www.exceptional.io/">http://www.exceptional.io/</a> [DEAD, acquired by Airbrake]</li>
<li><a href="http://www.bugsense.com/">http://www.bugsense.com/</a> [DEAD, acquired by Splunk]</li>
<li><a href="https://crashlog.io/">https://crashlog.io/</a> [DEAD]</li>
<li><a href="http://www.geterrorzero.com/">http://www.geterrorzero.com/</a> [DEAD]</li>
<li><a href="https://www.debuggify.net/">https://www.debuggify.net/</a> - source maps, tracekit [DEAD]</li>
<li><a href="http://www.errzero.com/">http://www.errzero.com/</a> [DEAD]</li>
<li><a href="http://qbaka.com/">http://qbaka.com/</a> [DEAD]</li>
<li><a href="http://www.exceptionhub.com/">http://www.exceptionhub.com/</a> [DEAD]</li>
<li><a href="https://errlytics.com/">https://errlytics.com/</a> [DEAD, announced service discontinuation on homepage]</li>
</ul>
<h2 id="contributing">Contributing</h2>
<p>Contributions welcome! Read the <a href="CONTRIBUTING.md">contribution guidelines</a> first.</p>

