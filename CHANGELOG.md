# Change Log

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/)
and this project adheres to [Semantic Versioning](http://semver.org/).

## [Unreleased]

### Fixed
- Too fast hiding of video settings menu (Vimeo) [RGOeX-26171]
- Captions toggling and displaying (HTML5)(Chrome/Safari) [RGOeX-26170]
- Progress line width exceeded video player limits (HTML5) [RGOeX-26169]
- Progress line width exceeded video player limits (Brightcove) [RGOeX-25758]
- Incorrect error message when uploading handouts in an unsupported format [RGOeX-26044]
- 500 error during upload hangout file [RGOeX-25995]

## Added
- Add transcripts auto-scrolling on play (RGOeX-26175)
- Update the README [xblock-video] (RGOeX-26032)

## [1.2.0] 2023-07-21

## Added
- Removed the "Default Timed Transcript Functionality" for HTML 5 Video Provider [xblock-video] (RGOeX-25745)
- Convert transcript file to .vtt format on manual upload [xblock-video] (RGOeX-25759)
- Implement Tencent super player [HARROW-976]

## [1.1.4] 2023-03-23

### Added
- Add the ability to set start and end times for video playback for the Brightcove player [RGOeX-25454]

## [1.1.3] 2023-03-21

### Fixed
- The link to download the subtitle file is missing href to the subtitle file [RGOeX-25430]
- Fix transcript appearing and controls buttons positioning for Brightcove player [xblock-video] (RGOeX-25698)
- Fix for download subtitles button under the video [xblock-video] (RGOeX-24475)

### Added
- Add base color to edit modal window [xblock-video] (RGOeX-25432)
- Add base color for subtitles list and player control buttons [xblock-video] (RGOeX-25440)

## [1.1.2] 2023-02-06

### Fixed
- Error during reading manually added subtitles [RGOeX-24483]

## [1.1.1] 2023-01-25

### Fixed
- fix: [RGOeX-1240] save scroll position on exit from fullscreen

## [1.1.0] 2022-09-12

### Fixed
- Fix BrightCove styling for players based on video.js v6+ (breaks video.js5 but that's very old now)
- a11y fix - title on video iframe
- Don't override account_id with a blank form value for new XBlock instances when value available from settings
- Added missing package data to fix installation without -e flag
- Updated requirements to be compatible with Maple release
- Remove player buttons focus outline (RGOeX-968)
- Set main theme color for Handout download button (RGOeX-981)
- Hide default big play button from wistia player (RGOeX-977)
- Minimize player button alignment fix (RGOeX-967)
- Fix speed dropdown width (RGOeX-651)
- Fix for videos aspect ratio and responsiveness (all providers) (RGOeX-980)
- Brightcove subtitles popup fix (RGOeX-976)
- Change color for focused items in the player speed dropdown (RGOeX-1344)
- Remove vjs controls from vimeo videos for avoiding problems with default vimeo controls (RGOeX-978)
- Save scroll position on exit from video xblock fullscreen mode (RGOeX-1240)

### Added

- Add support for the Nutmeg release [RGOeX-1644](https://youtrack.raccoongang.com/issue/RGOeX-1644)
  - bump requirements for pycaption and xblock-utils
  - this requires the edx-platform to update its requirements to use `lxml>=4.9` (current version is `4.5.0`) because of pycaption requirements.

## [1.0.1] - 2021-10-20

## Fixed

- Add support for Koa+ Open edX releases

## [0.10.1] - 2018-02-13

## Added

- Multiple transcripts downloading;
- Error handling during Brightcove video re-transcode job submitting;

## Fixed

- Safari `empty transcripts` issue;
- Studio editor improvements:
    - transcripts accordion switch;
    - re-transcode button styling;

## [0.10.0] - 2018-01-24

## Added

- Ability to perform search within text tracks (subtitles/transcripts);

### Fixed

- Player controls alignment;
- Active languages highlighting inconsistency between transcript and caption menus;

## [0.9.4] - 2018-01-18

### Fixed

- Language menu popup behaviour in player's subtitles/transcripts control group;
- Removed caret control from controls;
- Speed rates popup shifted;

## [0.9.3] - 2017-12-28

### Fixed

- Removed menu popup doubling in player's subtitles/transcripts control group.
- Updated python code quality configuration.

## [0.9.2] - 2017-11-03

### Fixed

- Edge / IE11 issues;
- Brightcove player ver. 6 layout:

>Brightcove player version 6 (videojs v.6 based) has introduced new css-styles and some decent API changes.

## [0.9.1] - 2017-08-04

### Changed

- Handouts: wide list of file types now is allowed to upload (please,
 refer to README file).
- UI: minor changes to default transcripts accordion section (appearance, wordings)
- Increase test coverage to improve product stability.
- Some code base refactoring to make xblock more robust.

### Fixed

- Brightcove player state handling
- Token field regression bug (accordion refactoring)

## [0.9.0] - 2017-07-11

### Added

- Direct transcripts streaming from 3PlayMedia service.
  Now Video Xblock will always use up-to-date transcripts from 3PM.

### Changed

- UI: Transcripts settings section now split into two panels.
  To make more apparent how different options are related and which
  transcripts are going to be diplayed.
  - "Manual & default transcripts"
  - "3PlayMedia transcripts"

## [0.8.0] - 2017-06-30

### Added

- Vimeo: default transcripts fetching.

## Changed

- Use new 3PlayMedia API to fetch transcripts translations.
- Increase test coverage. Which means better stability.

### Fixed

- Bug preventing setting Video Platform API key. E.g. `BC_TOKEN` for Brightcove.
- Transcripts collision bug, which prevented teachers to replace
  transcript for a given language.

## [0.7.1] - 2017-05-18

### Added

- Pass some debugging information to the front end.

## [0.7.0] - 2017-05-17

### Added

- XBlock SDK Workbench scenarios to simplify development.
- Acceptance tests on top of XBlock SDK Workbench.

### Removed

- Removed TravisCI integration.

## [0.6.6] - 2017-05-03

### Changed

- Make transcripts help hint more helpful.

## [0.6.5] - 2017-04-21

### Added

- Bundle VideoJS fonts into Video XBlock.

## [0.6.4] - 2017-04-14

### Changed

- Improve video player controls look&feel.
- Make subtitles responsive.

### Fixed

- Fetching subtitles from 3PlayMedia.

## [0.6.3] - 2017-03-30

### Changed

- Extend Brightcove url regex to include additional set of video urls.
  Now it supports both:
  - `https://studio.brightcove.com/products/videos/<media-id>`
  - `https://studio.brightcove.com/products/videocloud/media/videos/<media-id>`
- Restructure JavaScript codebase.

## [0.6.2] - 2017-03-27

### Changed

- Update `videojs-wistia` external JS dependency.

## [0.6.1] - 2017-03-27

### Changed

- Simplify VideoXBlock installation by bundling JS/CSS dependencies into
  `static/vendor` subdirectory.

## [0.6.0] - 2017-03-23

### Added

- 3PlayMedia support. Now you can fetch transcripts for your video from 3PM.
- Open edX settings support. Now administrators can set default values
  for VideoXBlock on a system-wide level.

### Changed

- Swith from Coveralls to Codecov for better code coverage.
- Interactive transcripts now align current line to the middle of video frame.

### Fixed

- Interactive transcripts automscrolling for Brightcove videos.

## [0.5.0] - 2017-03-14

### Added

- Html5 video support.
- Manual uploaded transcripts validation: file extension and size.
- Code stabilization:
  - Python unit tests.
  - JS unit tests foundation.

### Changed

- Interactive transcripts now automatically scroll to follow video.
- UI improvements in Studio:
  - Split Video XBlock settings into Basic & Advanced tabs.
  - Display only fields relevant to selected video.
- Move all python dependencies into setup.py to simplify XBlock installation.

### Fixed

- Various bugs.

## [0.4.0] - 2017-02-07

### Added

- Vimeo backend support
- Brightcove content protection and auto-quality
  - On API authentication uploads two custom Ingest Profiles:
    - Creates new API credentials with required permissions
    - HLS for auto quality
    - HLSe for auto qualify & encryption

- Add new UI controls after a user has authenticated against Brightcove API:
  - View video tech info.
  - Send video re-transcode request on a Brightcove side.

- Default transcripts upload:
  - Allows to fetch transcripts from the platform and store them into XBlock.
  - Supports: Brightcove, Youtube & Wistia.
  - Brightcove & Wistia require API authentication before default transcripts
  upload can work.

- Dev process improvements:
  - Code Climate integration to track code quality.
  - Coveralls.io integration to track test coverage.

### Changed

- Now TravisCI runs eslint and python unit tests on every commit.

### Fixed

- Various bugfixes and improvements.

## [0.3.0-alpha] - 2017-01-16

### Added

- SRT subtitles support.
- Transcripts downloading for students.
- TravisCI integration: pylint to begin with.

## Fixed

- Code cleanup.
- Various bugs.

## [0.2.0-alpha] - 2017-01-04

### Added

- Interactive transcripts.
- Closed captions.
- Open edX Analytic events.
- Brightcove playerID support.
- Handouts upload/download.
- Context menu.
- Offset start/end time.
- A11y: keyboard-only access, screen readers support.

## [0.1.0-alpha] - 2016-11-30

### Added

- Youtube support.
- Wistia support.
- Basic Brightcove support.
- Different playback rates support.
- Video player state load/save.
- All video players share skin similar to Open edX's video module.

[0.1.0-alpha]: https://github.com/raccoongang/xblock-video/tree/v0.1.0-alpha
[0.2.0-alpha]: https://github.com/raccoongang/xblock-video/compare/v0.1.0-alpha...v0.2.0-aplha
[0.3.0-alpha]: https://github.com/raccoongang/xblock-video/compare/v0.2.0-alpha...v0.3.0-aplha
[0.4.0]: https://github.com/raccoongang/xblock-video/compare/v0.3.0-alpha...v0.4.0
[0.5.0]: https://github.com/raccoongang/xblock-video/compare/v0.4.0...v0.5.0
[0.6.0]: https://github.com/raccoongang/xblock-video/compare/v0.5.0...v0.6.0
[0.6.1]: https://github.com/raccoongang/xblock-video/compare/v0.6.0...v0.6.1
[0.6.2]: https://github.com/raccoongang/xblock-video/compare/v0.6.1...v0.6.2
[0.6.3]: https://github.com/raccoongang/xblock-video/compare/v0.6.2...v0.6.3
[0.6.4]: https://github.com/raccoongang/xblock-video/compare/v0.6.3...v0.6.4
[0.6.5]: https://github.com/raccoongang/xblock-video/compare/v0.6.4...v0.6.5
[0.6.6]: https://github.com/raccoongang/xblock-video/compare/v0.6.5...v0.6.6
[0.7.0]: https://github.com/raccoongang/xblock-video/compare/v0.6.6...v0.7.0
[0.7.1]: https://github.com/raccoongang/xblock-video/compare/v0.7.0...v0.7.1
[0.8.0]: https://github.com/raccoongang/xblock-video/compare/v0.7.1...v0.8.0
[0.9.0]: https://github.com/raccoongang/xblock-video/compare/v0.8.0...v0.9.0
[0.9.1]: https://github.com/raccoongang/xblock-video/compare/v0.9.0...v0.9.1
[0.9.2]: https://github.com/raccoongang/xblock-video/compare/v0.9.1...v0.9.2
[0.9.3]: https://github.com/raccoongang/xblock-video/compare/v0.9.2...v0.9.3
[0.9.4]: https://github.com/raccoongang/xblock-video/compare/v0.9.3...v0.9.4
[0.10.0]: https://github.com/raccoongang/xblock-video/compare/v0.9.4...v0.10.0
[0.10.1]: https://github.com/raccoongang/xblock-video/compare/v0.10.0...v0.10.1
[Unreleased]: https://github.com/raccoongang/xblock-video/compare/v0.10.1...HEAD
