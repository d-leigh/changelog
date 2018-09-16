# changelog

# 0.0.7 (September 16th, 2018)

## New

![Screenshot](/images/report-award-section-0.0.7.png)

Added an `award` section to individual reports.

Added `user` gravatars to the report assignment field.

Added important report-related email notification triggers.

Added `/program scope` selection to individual reports.

Added icons that indicate type of change to a report's activity log.

Added [vue-lazyload](https://github.com/hilongjw/vue-lazyload) to images on `homepage` to improve page load time.

Added [redirect-ssl](https://www.npmjs.com/package/redirect-ssl) to improve `SSL` handling on older browser clients.

Added [Web Font Loader](https://github.com/typekit/webfontloader) to improve typeface handling.

Added URL redirection for `/reports/:id` upon successful `/sign-in`.

## Updated/Fixed

![Screenshot](/images/report-timeline-0.0.7.png)

Redesigned layout and styling for individual reports.

Implemented a friendlier report update interface.

Merged the submitted report and program's report into a single view.

Moved the report comment system into a single view.

Renamed `History` to `Timeline` for a report's activity log.

Changed `timestamp` format for a report's activity log.

Provided a method to collapse a report's activity log.

Compressed `homepage` images with `webp` to load on smaller screens.

Floated form-response notifications to improve visibility.

Switched `datetime` handling from [moment.js](https://github.com/moment/moment) to [date-fns](https://github.com/date-fns/date-fns).

## Removed

Removed option to edit an original report after it has been submitted.

Removed `user` gravatars from the report's activity log.

# 0.0.6 (August 20th, 2018)

## New

![Screenshot](/images/signup-password-strength-indicator-0.0.6.png)

Added a password strength indicator to the `/sign-up` page.

Added Sentry for better error-tracking and real-time fixes.

Added `Critical` as a priority level option for `/program scopes`.

Added 'Featured On' section to the landing page.

Added Open Graph tags.

## Updated/Fixed

Permitted Facebook and Twitter sharing from browser extensions.

Normalized `/login` to `/sign-up` and added redirect.

Fixed `user=researcher` differentiation in the `join` form on the landing page.

Desaturated logos on landing page, colorizing onHover.

Optimized images to improve landing page load-time.

Loosened input validation for `/program` name to allow `.`, `&` and `+`.

Improved validation for `email address` fields in `auth` forms.

Rearranged the 'invite to program' sections of the `/program` editor by hierarchy of `role` permissions.

Added error notification for exceeding invites while adding new users through the `/program` editor.

Updated `/report` comment style and added time since post.

Modified error notifications for edge cases to be more descriptive.

Fixed navigation from `/programs` to `/reports` to display inbox instead of the new report form.

Fixed a bug with adding and deleting `roles`.

Updated `/report` assignment to sync with API `role` changes.

Improved onboarding experience and emails.

Resolved rack-attack issue and re-enabled.

## Removed

Removed public user search field from the 'invite to program' sections of the `/program` editor.

# 0.0.5 (August 12th, 2018)

## New

![Screenshot](/images/report-inbox-donut-0.0.5.png)

A chart displaying report count by severity level has been added to the `/reports` inbox.

The scope tables for each `/program` utilizes a toggle to switch between in/out.

Added 404 page.

Soft deletion and soft dependency deletion for everything.

Sort scopes where they were missing (`created_at` asc).

Added a review process for programs to go public.

`GET api/roles` now returns `user_ids`.

## Updated/Fixed

![Screenshot](/images/program-scopes-slider-0.0.5.png)

The scope section of `/program` has a slick new theme.

Updated username and program name validation to limit types of characters accepted.

Fixed `user.invited_by` was not being set in some cases.

Fixed major issues with responsive mobile styling.

Fixed gravatars in `/reports` inbox to sync with assignee.

The CVSS rating module has been removed from all reports to simplify the submission process.

The required fields of a report can no longer be left empty or edited and resubmitted with blank content.

Fixed report assignment to allow selection of anyone given access within the program settings.

Fixed the visibility of new comments when a report is first reopened.

The `/reports` inbox now shows a custom message when returning zero results dependent on selected filter.

The login process has been optimized for faster load-time.

Implemented a fallback to ensure data is captured from the sign up form when the API is down.

## Removed

Overloading of invitations to allow multi-use invitations (this means an invitation can only be used once).

Remediations, we'll circle back on this feature when we have time to do it justice.

# 0.0.4 (August 7th, 2018)

## Updated/Fixed

![Screenshot](/images/program-page-redesign-0.0.4.png)

New styling applied to `/program` profiles

`/program` scopes moved from separate tabbed view to visible above the VDP

Copy changed in `/program` Rewards table from 'Vulnerability Type' to 'Vulnerability Level'

Made header sticky while scrolling `/program` VDP

Light style changes applied within the wysiwyg editor of the `/program` creation/update form

After submitting a report, you are now directed to the list of reports you have submitted instead of the dashboard's default view

## Known Issues

CSP can be improved and tightened

# 0.0.3 (August 2nd, 2018)

## New

![Screenshot](/images/report-inbox-0.0.3.png)

First pass at `/reports` re-design 

Critical priority for reports

Sqreen for Content Security Policy and other headers for `www.federacy.com`

[Vulnerability Disclosure Policy](https://github.com/federacy/vulnerability-disclosure-policy) posted to github using the Creative Commons Attribution Share Alike license. 

## Updated/Fixed

Template VDP Rewards Copy and Table

Clean up `/network` and invitations list

## Known Issues

CSP can be improved and tightened

# 0.0.2 (July 31st, 2018)

## New

Content Security Policy, CORs, and some denial of service mitigations for `api.federacy.com`

Password reset functionality

## Removed

Points as a scope reward, because this functionality has not yet implemented

## Updated/Fixed

Resolved ssues with invitations, roles, and reports

Improved policies, scopes, and routes to be more restrictive, and resolved a multitude of bugs created in the process

Improve email copy for invitations, activations, and signups

## Known Issues

rack-attack ip tracking using proxy addresses instead of end-user

invitations have been overloaded to support a single invitation being used many times (for HN post)

# 0.0.1 (July 11th, 2018)

Private alpha launch on Bookface!
