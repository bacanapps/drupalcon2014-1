#DrupalCon Amsterdam - Day 01#

##Drupal 8 - The Crash Course
30.09.2014 - 10:55
by Larry Garfield / palantir.net

htpps://gibhub.com/palantirnet/hugs

* The concepts are still Drupal
* The architecture is modernized
* The APIs are more consistent

Drupal in 2 steps:

1. Build a tool
2. Wire it up to the system

/modules/hugs/hugs.info.yml

name: Hugs
description: Examples of hugs
type: module
dependencies: 8.x


##The State of the Frontend
30.09.2014 - 13:00
by David Hwang, Brian Wald

####Yesterday

Front End changed, a lot.

Front End is pushing Drupal forward.

####Today

The post-responsive world

* Responsive (is expected)
* Touch
* Performant
* Javascript is cool again
* Multiple frameworks for everything
* Lots of powerful new toys

####Tomorrow

Lots of devices, lots of resolutions ...

Who's ready to make some dial-based front-ends?

#####The goal: truly device-independent design and development (headless, api driven drupal)

>"You'll be ahead, but only for a short time."
>Alan Watts, 1969

##Drupal 8 Contrib Module Status Update
30.09.2014 - 14:15

###1. Rules

####Under the hood
* Drupal 8 DX
* Plug-in system
* Entities, Typed data
* Deployable config via CMI

####Reusable components
* Context API shared w/ Core, Page Manager
* Tokens
* Typed data widgets & formatters
* Embeddable Rules UI compenents
  * Actions & Conditions
  * Rules data selector for tokens

####Site building
* Admin UI usability improvements
* Simple Views Bulk operations in core
* "Inline Rules" instead of Rule sets / Rules conditional

==> Fundraising (currently 18.000, needed 48.000 for 1.000 hrs)

==> Finished by beginning of 2015 (April?)

###2. Panels

* New Drupal 8 Page Manager
  https://www.drupal.org/project/page_manager
  Page Manager will be moved out of Panels
* Create a migration path from d7 page_manager to d8

=> #drupal-scotch on irc.freenode.net
=> @dsnopek, @japerry, @timplunkett

###3. Media
_by Dave Reid_

* drupal.org/project/entity_browser (very early stage of dev)
* drupal.org/project/media_entity
* drupal.org/project/entity_embed (totally usable; could only break if D8 changes)
* More embeds
 * Embed framework/API
 * URL embeds
 * Shortcode embeds
 * Field embeds
* drupal.org/project/file_entity
* drupal.org/project/fallback_formatter
* Other Components
 * File Image Formatters
 * Field Formatter

What happens with the Media/Scald module itself?
  => a module containing all the components will be worked on 

D8: File listings, multiple file uploads, embed images with WYSIWYG by default

###4. Search API
_by Thomas Seidl_

* Basic architecture unchanged
* Focus on flexibility and UX
 * Multiple item types per index
 * More components pluggable/configurable
  * Restrict index to specific bundles
* User Experience
 * Revised user interface
 * Revised terminology
 * Planned: Simpliefied UI / Wizard module
 * Planned: Tour module support

####Current Status
* Exisitng functionality ported
* A lot of improvements still to do
* Whole week sprint here at DrupalCon

###5. Commerce

Starting from scratch for d8
Mid 2015 release

###6. Display Suite
_by Bram (Aspilicious)_

* It was functional
* 80 % finished
* Do not *use* it yet
* Not yet in beta
* Will be done by the end of the year

##Getting your content to a mobile device in less than 1000ms
_by Iam Carrico_

https://iamcarrico.com

###Why?
* Bounce rates increase
* cannot rely on 4G
* many countries mobile only

Test everything when you change something

#####Tools
* Web Page Test
* YSlow
* PageSpeed
* Chrome's Dev Tools
* Casper.js

==> Session: Automated Frontend Testing

Get HTML, CSS and JS to render asap

#####Javascript
1. Move JavaScript to the footer
2. Utilize async /defer
3. Inline critical JS

1. and 2. use the Magic Module

#####CSS
1. Inline critical CSS (the fold is back)
2. Load the rest of CSS asyncronosly (LoadCSS)

=> There is no "out of the box" Drupal solution for this yet.

#####TCP
1. Latency is the issue not speed
One TCP request: 
Google Fibre: 220 - 280 ms
LTE: 400 - 500 ms
3G: 800 - 1000 ms

2. Use a CDNs
* We are limited by the speed of light
* Put your content closer to the user

3. First Packet Response
* RFC 6928: 10 packets
* 14.6 kb
* https://iamcarrico.com

4. HTTP 1.1 Tricks
* Domain sharding
* Concatenation
* Spriting
* Inlining of assets

5. HTTP 2.0 (ISH) => Prepare for SPDY
* Multiplexed streams
* Request prioritization
* Server push
* Removal of redundant headers
* Compressed headers

5. Tricks 2.0
* Do not use domain sharding
* Concatenation can hurt performance
* Utilize Server.push for important assets (SPDY module is in research)

6. iamcarrico.com
* Utilizes SPDY
* Has a custom CDN
 * Moved DNS to AWS Route 53
* Inlines critical CSS on first page load
* Loads rest of CSS asynchronously

7. Results
* PageSpeed: 98
* YSlow: 98
* Pingdom: 93 w/ sub 500 ms load time
* Web page test: 400-800 ms load time

####Q&A
* use progressive jpgs
* performance budgets
* constraints of the web include performance

##Drupal 8 Breakpoints and Responsive images
_by Peter Droogmans @attiks_

###HTML5 picture tag

The Polyfill for picture tag
https://guthub.com/scottjehl/picturefill
=> not supported by IE8

When to use 'picture'
* sizes
* dpi (retina)
* mime types
* art direction

When not to use picture
* small logo
* avatars
* ads / banners
* using svg

###Breakpoints
Also known as media queries, used to define when your layout has to been altered.
* Breakpoints used for the layout (grid) in your theme
* Breakpoints used for inline content

####Breakpoints for layout
Defined in temotheme.breakpoints.yml but not necessarily used by your sass or css.

####Responsive image mappings

####Possible solutions
* Old school: add more breakpoints
* New school: use sizes (third option: "Use the sizes attribute")