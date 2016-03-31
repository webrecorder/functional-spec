# webrecorder.io 
## Functional Specification

Webrecorder.io is an open source web archiving service.  Webcrecorder.io allows anyone to easily create high-fidelity, standards compliant archives of the web as they browse.  

For anonymous users, webrecorder.io provides
- an interface to record the web as you browse
- an interface to browse web recordings
- free, temporary archive hosting
- archive download in .warc format

For registered users, webrecorder.io also provides 
- permanent hosting of archives
- an interface to curate and share archives 

This document describes the interface and functionalities that are available through webrecorder.io.  It does not cover technical or implementation details, or details about the webrecorder platform or API.  Read all about the platform over at the [platform specification](http://github.com/webrecorder/platform-spec).  

This specification is a living document that is by no means complete or free of error.  Pull requests with corrections and improvements are most welcome!  Please send questions and suggestions to masha.lifshin@rhizome.org. 


## Table of Contents

1. Personas and scenarios
1. Glossary
1. Workflow diagram
1. Page-by-page mockups with very detailed descriptions
1. Table of canonical page names and their paths
1. Outstanding issues and future work


## Personas and Scenarios

## Glossary

- *recording*
- *collection*
- *archive*
- *page*
- *version*
- *to record*
- *to browse a recording*

## Workflow diagram


## Page by page mockups with very detailed descriptions

### Anonymous user recording workflow
1. New recording

##### Valid recording names
    we won't allow recording names of that are all digits or end in two letters followed by underscore

1. Recording in progress
1. Collection info
1. Browse recording

### Logged in user recording workflow
- New recording
- Recording in progress
- Collection info
- Browse my own recording 
- Browse someone else's recording

### Logged in user archive management
- Archive info

## Table of canonical page names and their paths

Canonical name | User | Path
---------------|------|----------
New recording | anon |   https://webrecorder.io
New recording | registered | 
| | |
| | |
Recording in progress | anon | https://webrecorder.io/anonymous/recording-name/record//http://example.com/
Recording in progress | registered | https://webrecorder.io/user/coll/recording-name/record//http://example.com/
| | |
| | |
Browse recording | anon | https://webrecorder.io/anonymous/recording-name//http://example.com/
Browse recording | registered | https://webrecorder.io/user/coll/recording-name/http://example.com/
| | |
| | |
Browse most recent page version | anon | https://webrecorder.io/anonymous/http://example.com/
Browse most recent page version  | registered | https://webrecorder.io/user/coll/http://example.com/
Browse page version closest to date | anon | https://webrecorder.io/anonymous/20160101000000/http://example.com/
Browse page version closest to date | registered | https://webrecorder.io/user/coll/20160101000000/http://example.com/
| | |
| | |
Collection info |  anon |  https://webrecorder.io/anonymous
Collection info | registered | https://webrecorder.io/user/coll/
Recording info | anon | https://webrecorder.io/anonymous/recording-name  
Recording info | registered | https://webrecorder.io/user/coll/recording-name 
| | |
| | |
Archive info | registered | https://webrecorder.io/user
Account settings | registered | https://webrecorder.io/user/_settings
| | |
| | |
Live preview | debug | https://webrecorder.io/live/http://example.com/

## Outstanding issues and future work

- Create an interface where you can get a time based list of all recordings in a collection that contain a page.  The path to this functionality would be https://webrecorder.io/anonymous/*/http://example.com/ for anonymous users and https://webrecorder.io/user/coll/*/http://example.com/ for registered users.
