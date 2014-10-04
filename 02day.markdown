#DrupalCon Amsterdam - Day 02#

##Keynote: Cory Doctorow
01.10.2014 - 09:00
_Cory Doctorow (craphound.com)_

##Render Caching in Drupal 7 and 8
01.10.2014 - 10:45

https://amsterdam2014.drupal.org/session/render-caching-drupal-7-and-8

Module: render_cache

The problem: building and rendering entitites can be slow

###How to use it
* includes with comments, context, ds, nodes, views
* works with custom entities

###Caveats
* embedded entities
* think in entities
* permanent cache

###Fastest drupal ever

render_cache-7.x-2.x-dev

##GitHub Pull Request Builder for Drupal
01.10.2014 - 13:00

GitHub

Jenkins

Run CasperJS Tests
Take screenshots with Resemble.js

Tugboat

##Future-Proof your Drupal 7 site
_by Dave Reid_

@davereid
davereid.github.io/future-proof

###Modules in D8
>also available for D7 (as backports)

####Spark
[https://www.drupal.org/project/spark]

####Navbar
[https://www.drupal.org/project/navbar]

####Inline Editing
[https://drupal.org/project/quickedit]

####CK Editor
[https://drupal.org/project/ckeditor]

####Responsive Bartik
[https://drupal.org/project/responsive_bartik]

####HTML5 Tools
[https://drupal.org/project/elements]
[https://drupal.org/project/html5_tools]
HTML5 input elements

####Views in Core
[https://drupal.org/project/views]

####Admin Views
[https://drupal.org/project/admin_views]

####Views Bulk Operations (Light)
[https://drupal.org/project/views_bulk_operations]

####Views Responsive Grid
[https://drupal.org/project/views_responsive_grid]

####Responsive Tables
[https://drupal.org/project/responsive_tables]

####Breakpoints
[https://drupal.org/project/breakpoints]

####Responsive Images
[https://drupal.org/project/picture]

####Tours
[https://drupal.org/project/joyride]

####Module page filtering
[https://drupal.org/project/instantfilter]

####Simpliefied Menu Administration
[https://drupal.org/project/simplified_menu_admin]

####Escape Admin
[https://drupal.org/project/escape_admin]

####Caption Filter
[https://drupal.org/project/caption_filter]

####Bean
[https://drupal.org/project/bean]
Let's you make custom blocks with fields

####Multi Blocks
[https://drupal.org/project/multiblock]
Let's you create multiple instants of a block

####Entity reference
[https://drupal.org/project/entityreference]
>the module for reference (don't use node reference)

####Telephone
[https://drupal.org/project/telephone]
>Better than the phone module

####Email
[https://drupal.org/project/email]

####Datetime
[https://drupal.org/project/date]  
>Use the Date (ISO format) field type

####UUIDs
[https://www.drupal.org/project/uuid]

####Render Cache
[https://www.drupal.org/project/render_cache]  
[https://www.drupal.org/project/entity_modified]
>especially if you have a lot of logged in users

####For developers
#####Composer
 [https://getcomposer.org/]
#####API and Plugins
 see slides

####Configurable view/display modes
[https://drupal.org/project/entity_view_mode]  
>can be cached easily; use it  
>DS will probably be depracated in D8

####CMI
[https://drupal.org/project/configuration]

####Migrate is your friend
[https://drupal.org/project/migrate]  
[https://drupal.org/project/migrate_d2d]

####RESTful Web Services

####Translation
[https://drupal.org/project/entity_translation]  
[https://drupal.org/project/title]

####Distribution: PreD8
[https://www.drupal.org/project/pred8]

####Modules and themes removed from core in Drupal 8
[https://www.drupal.org/node/2116417]

##Managing Complex Projects With Design Components
01.10.2014 - 15:45
_by John Albin_

[Video and Slides download] (https://amsterdam2014.drupal.org/session/styleguide-driven-development-new-web-development)

Goal: explain AGILE

Web Components:  
Agile Development requires Continuous Integration  
Component Library are documented by style guides  

Agile tries to reduce your risk (as opposed to the waterfall model)

Agile project => Sprint

Grab the first two Features and implement them in the first sprint.
After first sprint re-prioritize the features.

Each 2-week sprint:
* Prioritizes project goals
* Completes a set of features

Agile + Web = Component-based desig + Automated style guides  
==> *Styleguide-driven development: The new web development*  
Only requirements are: *Component-based design* and *Automated style guides*

Problems:
* CSS specifity wars
* Overly generic class names

####What is a design component?

* "Object" in OOCSS
* "Module" in SMACCS
* "Block" in BEM's Block-Element-Modifier
* "UI Pattern"

####CSS Design components are:

* Applied to a loose collection of HTML elements
* Repeatable 
* Self-contained
* Nestable

####SMACSS
1. Base =>   1. Base
2. Layout => 2. Layout
3. Module => 3. Components
4. State      3.1 Component
5. Theme      3.2 Element
              3.3 Modifier
              3.4 State
              3.5 Skin

.flower (component)
.flower__petals (element)
.flower__face
.flower__bed
.flower--tulip (modifier)
.flower:hover (state)
.flower.is-pollinating (state)
@media (min-width: 48em) { .flower } (state)
.is-night.flower (skin: global modifier)

Don't infer html structure with class names.

* Content semantics are handled by HTML5 elements
* Let's make our class names use Design semantics
* Class names should be meaningful to developers and designers

.the-component
.the-component--modifier
.the-component__an-element
.the-component--modifier__an-element
.the-component.is-state
 .the-component:hover
.the-skin .the-component

####Drupal CSS coding standards
www.drupal.org/node/1886770

####The "Fugly" Selector hack

####Automated Style Guide: KSS-Node
github.com/kss-node/kss-node

##The Future of HTML and CSS
01.10.2014 - 17:00  
https://amsterdam2014.drupal.org/session/future-html-and-css