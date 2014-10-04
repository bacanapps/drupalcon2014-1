#DrupalCon Amsterdam - Day 03#

##Coder vs. Themer Ultimate Grudge Smackdown Fight to the Death!
02.10.2014 - 10:45
_by Adam Juran and Campbell Vertesi_
[DrupalCon](https://amsterdam2014.drupal.org/session/coder-vs-themer-ultimate-grudge-smackdown-fight-death)

[wireframe](http://git.io/cvst)

##Automated Performance Tracking
02.10.2014 - 13:00
_by Fabian Franz aka Fabianx, @fabianfranz

[DrupalConAmsterdam Session website] (https://amsterdam2014.drupal.org/session/automated-performance-tracking)

* Performance is a very important factor in todays web-sphere
* Sub 1.0s goal for mobile
* Google penalty for slower pages
* Studies schowing users buying less if pages load too long

>Plan performance at the start of a project

####Performance Gate
* Great gate, but only works based onn individuals motivation.
* Cannot be enforced, because it cannot be measured

It's the small things that slows your site down not the big changes.  

####Current Performance Tracking
* How long does the test suite take?
* Is ab -n on average the same?
* Only for certain obvious issues, e.g. theme layer.
* Missing all real and hidden performance regressions.

It only became apparent that D8 got slower in comparison to D7.  
[current performance tracking] (https://www.drupalorg./project/webprofiler)  
a good start but not enough  
* Only for Drupal core
* Clients sites can be way different
* e.g. drupal_find_theme_functions() taking 300 ms on core and 3.5s on a client site

####Interesting Questions
>which cannot be answered so easily

* Is Drupal 8 slower than D7 at the back-end?
* What about front-end performance?
* How many database calls does D8 make per request?
* How many bytes are transfered by average?

###Automating the process
>to get understanding of site performance

####Backend-Automization

* *XHProf-Kit + XHProf-Lib*
* Measured every single patch for the twig theme conversions
* Revealed lots of performance problmes elsewhere, too
* Still very painful and hard work

####What is automated perfomance tracking?

* Not linear, but a tree structur
* What to track?
 * Time / Speed / Performance (raw)
 * Average
 * Quantitative (Numer fo Cache hits, file system accesses)
 * Quality (quality of aggregates => difficult to define)

####Front-End: prameters and measures

* Time-to-First-Byte
* Parse HTML / Parse CSS / Parse JS
* Execute Javascript
* Document.Ready() => More JS
* Window.Load() -> More JS
* First load time - no assets cached
* Facebook Big Pipe
* try out: ?big_pipe=flush_all?
* HAR (Http Archive 1.2 files)
* Browser-Timing API
* Webpagetest.org / Google Page Speed

####Back-End

* Render-Cache: Cache Hits vs Cache Misses
* Rebuilding time of important caches
* Apache Benchmark
* X Debug
* XHProf-Kit
* Symfony Debug Console
* strace
* Slow Query log => percona: pt-query-digest
* MySQL-Tuner.pl

* jMeter - load testing
* HAR - load testing
* behat -load testing

*==> use the test suite*  
[test suite](https://www.drupal.org/project/simpletest)

[behat] (http://docs.behat.org/en/v2.5/)

>sensiolabs profiler

##FIELD API IS DEAD. LONG LIVE ENTITY FIELD API!
_by Kristof De Jaeger - @swentel; Yves Chedemois - ; Wolfgang Ziegler - @the-real-fago
02.10.2014 - 14:15  
[DrupalCon Session](https://amsterdam2014.drupal.org/session/field-api-dead-long-live-entity-field-api)

####Site building features

* More power for site builders out of the box
* Not always full ports of the corresponding D7 modules
* Entity reference in core
* Date / Datetime in core
* Fieldable blocks

Cheat sheet

####Entities

