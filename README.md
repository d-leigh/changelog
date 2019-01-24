# Federacy Changelog

*[[1.1.0]] , 
[[1.0.0]] , 
[[0.0.12]] , 
[[0.0.11]] , 
[[0.0.10]] , 
[[0.0.9]] , 
[[0.0.8]] , 
[[0.0.7]] , 
[[0.0.6]] , 
[[0.0.5]] , 
[[0.0.4]] , 
[[0.0.3]] , 
[[0.0.2]] , 
[[0.0.1]]*

[1.1.0]: #110-january-23rd-2019
[1.0.0]: #100-january-19th-2019
[0.0.12]: #0012-december-10th-2018
[0.0.11]: #0011-december-1st-2018
[0.0.10]: #0010-november-6th-2018
[0.0.9]: #009-october-24th-2018
[0.0.8]: #008-october-11th-2018
[0.0.7]: #007-september-16th-2018
[0.0.6]: #006-august-20th-2018
[0.0.5]: #005-august-12th-2018
[0.0.4]: #004-august-7th-2018
[0.0.3]: #003-august-2nd-2018
[0.0.2]: #002-july-31st-2018
[0.0.1]: #001-july-11th-2018


<br/>&nbsp;


## 1.1.0 (January 23rd, 2019)


### Added

- in-place editing for `/program` VDP with Markdown support

- `/sign-up` notification of existing user account

- error notification during `/program` creation if `slug` is taken

- usernames and gravatars of `users` invited to `/program`

- researchers can be invited to `/program` by email address


### Changed

- migrated from HTML to Markdown for VDP copy

- `updated_at` attributes touched when children objects are updated/created

- `/program` roles and scopes editable in-place


### Removed

- `/program` setup access after program creation

- `program_name` and `slug` editing within UI


### Fixed

- "All Programs" filter in `/reports` to include programs to which you have reported regardless of current role

- resolution of URL redirection through `/sign-in`

- `payment history` of reports awarded by you that were submitted to programs you are no longer active in

- `payment history` of awards issued by your teammates

- change periods to dashes in `slug` if present in `program_name`

- `/researcher` profiles with `null` attributes are visible

- `submitted report` can be viewed even if `program` has been `deleted`

- `program` contract acceptance validation


### Security

- require ASCII-only URLs to mitigate IDN homograph vulnerabilities  
_reported by reymarkdivino_

- stronger password validation throughout site to improve user security (HIBP integration)


### Design

- mobile UI and copy tweaks

- VDP beautification

- redirection flow (routing) improvements upon `/sign-in` or revisiting `/` during session

- information display and UX improvements for `/researchers` list and `/researcher` profiles


### Policies

- timeliness notice appended to `new report` email notification

- user agreements and policies communicated during program setup and researcher onboarding available in [help center]

[help center]: https://help.federacy.com


### Known Issues

- session not invalidated on email address or password change


<br/>


## 1.0.0 (January 19th, 2019)


### Added

- program and researcher guided setup **[[1.0.0-01]]**

- user sessions with httpOnly cookies & CSRF tokens

- email address confirmation requirement

- performance metrics & launch date in `/programs` list **[[1.0.0-02]]**

- tabbed navigation to `/program` profiles

- "known issues" editor to `/program` profiles

- payment handling for programs to issue awards **[[1.0.0-03]]**

- new columns in `/reports` inbox

- "payment history" feed to `/payments` **[[1.0.0-04]]**

[1.0.0-01]: ./images/onboarding-selection-screen-1.0.0.png
[1.0.0-02]: ./images/programs-page-metrics-1.0.0.png
[1.0.0-03]: ./images/report-award-payment-modal-1.0.0.png
[1.0.0-04]: ./images/payments-payment-history-1.0.0.png


### Updated

- "awards" table moved from VDP to its own section **[[1.0.0-05]]**

- scopes table redesigned & editing simplified **[[1.0.0-06]]**

- program roles reconfigured

- filters applied in `/reports` inbox persist while browsing

- weekly reporting cap lifted once researcher is "vetted" by system **[[1.0.0-07]]**

- hyperlinked URLs in researcher's `/report` view

- "password change" functionality moved into modal **[[1.0.0-08]]**

- form field validations & alerts have been improved

- new theme for `/researcher` profiles **[[1.0.0-09]]**

[1.0.0-05]: ./images/program-awards-table-1.0.0.png
[1.0.0-06]: ./images/program-editor-scopes-setup-1.0.0.png
[1.0.0-07]: ./images/researcher-onboarding-reporting-limits-update-1.0.0.png
[1.0.0-08]: ./images/account-change-password-modal-1.0.0.png
[1.0.0-09]: ./images/researcher-profile-redesign-1.0.0.png


### Removed

- `/network` invites outside of programs

- tabbed `/program` editor

- wysiwyg VDP editor in `program` editor

- `/program` gravatars

- public visibility toggle in `/program` editor

- payout options for researchers other than PayPal

- waitlist for new program sign-up

- subscription plans for private programs


### Fixed

- public visibility toggle in `/profile` editor

- `submitted report` status displayed to the researcher


### Security

- various `IDOR` vulns identified and remediated  
	_reported by reymarkdivino_

- improperly repaired `SPF misconfiguration` remedied  
	_reported by japz_

- `unsafe-inline` resolved for CSP `script-src` & `style-src`  
	_reported by ali_


### Known Issues

- session not invalidated on email address or password change


<br/>&nbsp;


## 0.0.12 (December 10th, 2018)


### Added

- Added more filters to `/reports` inbox. **[[0.0.12-01]]**

- Added `awarded` column to `/reports` inbox tabular data.

- Added ability for program maintainers to submit and triage their own reports.

[0.0.12-01]: ./images/report-inbox-new-filters-and-awarded-column.png


### Updated/Fixed

- Fixed occasional empty `status` upon report creation.

- Refined filtering of reports by `status` in `/reports` inbox.


### Removed

- Removed report submission button from `/reports` inbox.


### Known Issues

- A notification email indicating your `password` has been changed is triggered when any `/account` settings are updated.

- The `program` visibility mechanics can be improved.

- The `reward` interface of a `program report` can be improved.


<br/>&nbsp;


## 0.0.11 (December 1st, 2018)


### Added

- Added internal `admin` controls and views.

- Added unsaved changes alert when navigating from `report`.

- Added notice about brevity to transactional emails.


### Updated/Fixed

- Moved `program report` field descriptions to tooltips. **[[0.0.11-01]]**

- Addressed state issues after updating `report` severity or status.

- Improved `report` editing interface.

- Improved navigation from `report` back to `/reports` inbox.

- Separated `/account` settings from `/profile` editor.

- Fixed formatting of blog hyperlink on `researcher profile`.

- Fixed website hyperlink redirect loop on `program` pages.

- Changed formatting of original `report` to render line breaks.

[0.0.11-01]: ./images/report-tooltips-and-editing.png


### Security

- Fixed bypassing homograph attack using /@.  
	_reported by reymarkdivino_


### Known Issues

- A notification email indicating your `password` has been changed is triggered when any `/account` settings are updated.

- The `program visibility` mechanics can be improved.

- The `reward` interface for a `report` can be improved.

- Program maintainers do not have access to the `report` options panel for reports they submit to their own program.


<br/>&nbsp;


## 0.0.10 (November 6th, 2018)


### Updated/Fixed

- Fixed formatting for `program report` when in read-mode.


### Security

- Made `invitation` codes single-use to prevent limit bypass.  
	_reported by reymarkdivino_

- Addressed homograph attack vulnerability.  
	_reported by reymarkdivino_

- Fixed invitation token leakage via referer header.  
	_reported by reymarkdivino_

- Remediated open redirect weakness.  
	_reported by ali_


### Known Issues

- A notification email indicating your `password` has been changed is triggered when any `user settings` are updated.

- Hyperlinks missing protocol in the url do not resolve to external website.

- The `program report` editing experience can be improved.

- The `reward` interface can be improved.


<br/>&nbsp;


## 0.0.9 (October 24th, 2018)


### Added

- Added pagination to `/researchers` page.

- Added field to select number of items displayed on `/researchers` page.

- Added URL persistence through sign-in for authenticated routes.

- Added container overflow control for `description` section of report content.


### Updated/Fixed

- Changed copy in various components and modules to improve UX.

- Fixed form interaction and `update` notifications in `/programs` editor.

- Improved responsive design of report pages on mobile devices.

- Addressed report `activity` logging bug that occasionally posted incorrect action.

- Fixed `gravatar` displayed for awarder of bounty in `activity` log of a report.

- Updated program invite-related mailers with minor copyedits.

- Switched mailers to send from `team@federacy.com` for better support handling.


### Removed

- Removed `Create Program` button from the UI for researchers.

- Removed `/network` page access for `inactive` users.

- Removed firing of notification mailers for a program's auto-generated example report.


### Known Issues

- A notification email indicating your `password` has been changed is triggered when any `user settings` are updated.

- The `reward` interface can be improved.


<br/>&nbsp;


## 0.0.8 (October 11th, 2018)


### Added

- Added section to the `/profile` editor below `user settings` for researchers to complete. **[[0.0.8-01]**

- Added `/billing` page with subscription plans.

- Added public `/researchers` list for subscribers with `search` and `filter` functionality. **[[0.0.8-02]**

- Added public researcher profiles accessible from `/researchers` list for subscribers.

- Added ability to `invite` a researcher to your `/program` from `/researchers` list and their corresponding profile page.

[0.0.8-01]: ./images/profile-editor-0.0.8.png
[0.0.8-02]: ./images/researcher-profile-0.0.8.png


### Updated/Fixed

- Fixed `/network` table styling.

- Renamed `visibility` field in `/profile` editor to clarify its function.

- Moved `visibility` toggle from `user settings` to `researcher profile` section of `/profile` editor.

- Updated `users` endpoint to include connected `users` through `programs` and `reports`.

- Fixed missing `user activation` mailers.

- Redesigned layout and styling for individual `reports`. **[[0.0.8-03]]**

- Moved `Award` section to `Reward` action that opens a modal in individual `reports`.

- Merged the `comment` system into a single module in individual `reports`.

- Combined the submitted report and program's report into a single panel that is switchable via link.

- Renamed `Timeline` to `Activity` in individual `reports`.

[0.0.8-03]: ./images/report-view-0.0.8.png


### Removed

- Removed `role.gravatar` from `api/roles`.

- Removed ability for `inactive users` to send invitations through the `/network` page.

- Removed ability for `inactive users` to make their profile `public`.

- Removed ability for researchers to `create programs`.

- Removed `priority` selection from individual `reports`.


### Known Issues

- A notification email indicating your `password` has been changed is triggered when any `user settings` are updated.

- The `reward` user interface can be improved and does not account for `swag` rewards.


<br/>&nbsp;


## 0.0.7 (September 16th, 2018)


### Added

- Added an `award` section to individual reports. **[[0.0.7-01]]**

- Added `user` gravatars to the report assignment field.

- Added important report-related email notification triggers.

- Added `/program scope` selection to individual reports.

- Added icons that indicate type of change to a report's activity log.

- Added [vue-lazyload](https://github.com/hilongjw/vue-lazyload) to images on `homepage` to improve page load time.

- Added [redirect-ssl](https://www.npmjs.com/package/redirect-ssl) to improve `SSL` handling on older browser clients.

- Added [Web Font Loader](https://github.com/typekit/webfontloader) to improve typeface handling.

- Added URL redirection for `/reports/:id` upon successful `/sign-in`.

[0.0.7-01]: ./images/report-award-section-0.0.7.png


### Updated/Fixed

- Redesigned layout and styling for individual reports.

- Implemented a friendlier report update interface. **[[0.0.7-02]]**

- Merged the submitted report and program's report into a single view.

- Moved the report comment system into a single view.

- Renamed `History` to `Timeline` for a report's activity log.

- Changed `timestamp` format for a report's activity log.

- Provided a method to collapse a report's activity log.

- Compressed `homepage` images with `webp` to load on smaller screens.

- Floated form-response notifications to improve visibility.

- Switched `datetime` handling from [moment.js] to [date-fns].

[moment.js]: https://github.com/moment/moment
[date-fns]: https://github.com/date-fns/date-fns

[0.0.7-02]: ./images/report-timeline-0.0.7.png


### Removed

- Removed option to edit an original report after it has been submitted.

- Removed `user` gravatars from the report's activity log.


<br/>&nbsp;


## 0.0.6 (August 20th, 2018)


### Added

- Added a password strength indicator to the `/sign-up` page. **[[0.0.6-01]]**

- Added Sentry for better error-tracking and real-time fixes.

- Added `Critical` as a priority level option for `/program scopes`.

- Added 'Featured On' section to the landing page.

- Added Open Graph tags.

[0.0.6-01]: ./images/signup-password-strength-indicator-0.0.6.png


### Updated/Fixed

- Permitted Facebook and Twitter sharing from browser extensions.

- Normalized `/login` to `/sign-up` and added redirect.

- Fixed `user=researcher` differentiation in the `join` form on the landing page.

- Desaturated logos on landing page, colorizing onHover.

- Optimized images to improve landing page load-time.

- Loosened input validation for `/program` name to allow `.`, `&` and `+`.

- Improved validation for `email address` fields in `auth` forms.

- Rearranged the 'invite to program' sections of the `/program` editor by hierarchy of `role` permissions.

- Added error notification for exceeding invites while adding new users through the `/program` editor.

- Updated `/report` comment style and added time since post.

- Modified error notifications for edge cases to be more descriptive.

- Fixed navigation from `/programs` to `/reports` to display inbox instead of the new report form.

- Fixed a bug with adding and deleting `roles`.

- Updated `/report` assignment to sync with API `role` changes.

- Improved onboarding experience and emails.

- Resolved rack-attack issue and re-enabled.


### Removed

- Removed public user search field from the 'invite to program' sections of the `/program` editor.


<br/>&nbsp;


## 0.0.5 (August 12th, 2018)


### Added

- A chart displaying report count by severity level has been added to the `/reports` inbox. **[[0.0.5-01]]**

- The scope tables for each `/program` utilizes a toggle to switch between in/out.

- Added 404 page.

- Soft deletion and soft dependency deletion for everything.

- Sort scopes where they were missing (`created_at` asc).

- Added a review process for programs to go public.

- `GET api/roles` now returns `user_ids`.

[0.0.5-01]: ./images/report-inbox-donut-0.0.5.png


### Updated/Fixed

- The scope section of `/program` has a slick new theme. **[[0.0.5-02]]**

- Updated username and program name validation to limit types of characters accepted.

- Fixed `user.invited_by` was not being set in some cases.

- Fixed major issues with responsive mobile styling.

- Fixed gravatars in `/reports` inbox to sync with assignee.

- The CVSS rating module has been removed from all reports to simplify the submission process.

- The required fields of a report can no longer be left empty or edited and resubmitted with blank content.

- Fixed report assignment to allow selection of anyone given access within the program settings.

- Fixed the visibility of new comments when a report is first reopened.

- The `/reports` inbox now shows a custom message when returning zero results dependent on selected filter.

- The login process has been optimized for faster load-time.

- Implemented a fallback to ensure data is captured from the sign up form when the API is down.

[0.0.5-02]: ./images/program-scopes-slider-0.0.5.png


### Removed

- Overloading of invitations to allow multi-use invitations (this means an invitation can only be used once).

- Remediations, we'll circle back on this feature when we have time to do it justice.


<br/>&nbsp;


## 0.0.4 (August 7th, 2018)


### Updated/Fixed

- New styling applied to `/program` profiles **[[0.0.4-01]]**

- `/program` scopes moved from separate tabbed view to visible above the VDP

- Copy changed in `/program` Rewards table from 'Vulnerability Type' to 'Vulnerability Level'

- Made header sticky while scrolling `/program` VDP

- Light style changes applied within the wysiwyg editor of the `/program` creation/update form

- After submitting a report, you are now directed to the list of reports you have submitted instead of the dashboard's default view

[0.0.4-01]: ./images/program-page-redesign-0.0.4.png


### Known Issues

- CSP can be improved and tightened


<br/>&nbsp;


## 0.0.3 (August 2nd, 2018)

- First pass at `/reports` re-design **[[0.0.3-01]]**

- Critical priority for reports

- Sqreen for Content Security Policy and other headers for `www.federacy.com`

- [Vulnerability Disclosure Policy] posted to github using the Creative Commons Attribution Share Alike license. 

[Vulnerability Disclosure Policy]: https://github.com/federacy/vulnerability-disclosure-policy

[0.0.3-01]: ./images/report-inbox-0.0.3.png


### Updated/Fixed

- Template VDP Rewards Copy and Table

- Clean up `/network` and invitations list


### Known Issues

- CSP can be improved and tightened


<br/>&nbsp;


## 0.0.2 (July 31st, 2018)


### Added

- Content Security Policy, CORs, and some denial of service mitigations for `api.federacy.com`

- Password reset functionality


### Removed

- Points as a scope reward, because this functionality has not yet implemented


### Updated/Fixed

- Resolved ssues with invitations, roles, and reports

- Improved policies, scopes, and routes to be more restrictive, and resolved a multitude of bugs created in the process

- Improve email copy for invitations, activations, and signups


### Known Issues


- rack-attack ip tracking using proxy addresses instead of end-user

- invitations have been overloaded to support a single invitation being used many times (for HN post)


<br/>&nbsp;


## 0.0.1 (July 11th, 2018)

- Private alpha launch on Bookface!
