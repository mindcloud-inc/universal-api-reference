# Zoho PageSense: Native API Reference

A consolidated summary of Zoho PageSense's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://www.zoho.com/pagesense/developerguide/apidocs/absplittestoverview.html
- **API base URL:** `https://pagesense.zoho.com/pagesense/rest/v1`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.zoho.com/oauth/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://accounts.zoho.com/oauth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `PageSense.experiments.CREATE,PageSense.experiments.READ,PageSense.experiments.UPDATE,PageSense.goals.CREATE,PageSense.goals.READ,PageSense.goals.UPDATE,PageSense.goals.DELETE,PageSense.audience.READ,PageSense.audience.UPDATE,PageSense.reports.all,PageSense.customevents.CREATE,PageSense.customevents.READ`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://accounts.zoho.com/oauth/v2/token.

[Official authentication documentation](https://www.zoho.com/accounts/protocol/oauth/web-server-applications.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `data_per_page` in the request body to set the page size. Use `page_number` in the request body to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort_by` in the request body. Set the direction separately with `sort_type`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Custom Event](actions/create-custom-event.md) | `POST /portal/:portalName/customevents` | [docs](https://www.zoho.com/pagesense/developerguide/apidocs/createeventsapi.html) |
| [Create Experiment](actions/create-experiment.md) | `POST /portal/:portalName/experiments` | [docs](https://www.zoho.com/pagesense/developerguide/apidocs/createabsplittest.html) |
| [Create Goal for Experiment](actions/create-goal-for-experiment.md) | `POST /portal/:portalName/goals` | [docs](https://www.zoho.com/pagesense/developerguide/apidocs/creategoalsabsplittest.html) |
| [Create Project Goal](actions/create-project-goal.md) | `POST /portal/:portalName/projectgoals/:projectLinkname` | [docs](https://www.zoho.com/pagesense/developerguide/apidocs/creategoals.html) |
| [Day-Wise Stats Reports](actions/day-wise-stats-reports.md) | `POST /portal/:portalName/fulltrackingreports` | [docs](https://www.zoho.com/pagesense/developerguide/apidocs/daywisestatsreport.html) |
| [Delete Goal for Experiment](actions/delete-goal-for-experiment.md) | `DELETE /portal/:portalName/goals/:goalLinkname` | [docs](https://www.zoho.com/pagesense/developerguide/apidocs/deletinggoalsabsplittest.html) |
| [Delete Project Goal](actions/delete-project-goal.md) | `DELETE /portal/:portalName/projectgoals/:projectLinkname` | [docs](https://www.zoho.com/pagesense/developerguide/apidocs/deletegoalsapi.html) |
| [Get Experiment Details](actions/get-experiment-details.md) | `GET /portal/:portalName/experiments/:experimentLinkname` | [docs](https://www.zoho.com/pagesense/developerguide/apidocs/fetchabsplittest.html) |
| [Get Project Goals](actions/get-project-goals.md) | `GET /portal/:portalName/projectgoals/:projectLinkname` | [docs](https://www.zoho.com/pagesense/developerguide/apidocs/fetchgoalsapi.html) |
| [Individual Stats Report](actions/individual-stats-report.md) | `POST /portal/:portalName/fulltrackingreports` | [docs](https://www.zoho.com/pagesense/developerguide/apidocs/individualstatsreport.html) |
| [List Custom Events](actions/list-custom-events.md) | `GET /portal/:portalName/customevents` | [docs](https://www.zoho.com/pagesense/developerguide/apidocs/fetcheventsapi.html) |
| [List Predefined & Custom Audiences](actions/list-predefined-custom-audiences.md) | `GET https://pagesense.zoho.com/pagesense/api/v1/portal/:portalName/audiences` | [docs](https://www.zoho.com/pagesense/developerguide/apidocs/audienceabsplittest.html) |
| [List Selected Audiences](actions/list-selected-audiences.md) | `GET https://pagesense.zoho.com/pagesense/api/v1/portal/:portalName/audiences` | [docs](https://www.zoho.com/pagesense/developerguide/apidocs/selectedaudienceexpt.html) |
| [Publish Experiment](actions/publish-experiment.md) | `PUT /portal/:portalName/experiments/:experimentLinkname/publish` | [docs](https://www.zoho.com/pagesense/developerguide/apidocs/publishexpts.html) |
| [Total Stats Report](actions/total-stats-report.md) | `POST /portal/:portalName/fulltrackingreports` | [docs](https://www.zoho.com/pagesense/developerguide/apidocs/totalstatsreport.html) |
| [Update Experiment Audience](actions/update-experiment-audience.md) | `PUT https://pagesense.zoho.com/pagesense/api/v1/portal/:portalName/experimentaudience/:experimentLinkname` | [docs](https://www.zoho.com/pagesense/developerguide/apidocs/updateexptaudience.html) |
| [Update Experiment Variations](actions/update-experiment-variations.md) | `PUT /portal/:portalName/experiments/:experimentLinkname` | [docs](https://www.zoho.com/pagesense/developerguide/apidocs/updateabsplittest.html) |
| [Update Goal for Experiment](actions/update-goal-for-experiment.md) | `PUT /portal/:portalName/goals/:goalLinkname` | [docs](https://www.zoho.com/pagesense/developerguide/apidocs/updategoalsabsplittest.html) |
| [Update Project Goal](actions/update-project-goal.md) | `PUT /portal/:portalName/projectgoals/:projectLinkname` | [docs](https://www.zoho.com/pagesense/developerguide/apidocs/updategoalsapi.html) |
