# changelog

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
