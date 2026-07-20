# Strategypoint: Native API Reference

A consolidated summary of Strategypoint's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://developer.clearpointstrategy.com/reference
- **OpenAPI specification:** https://apidoc.clearpointstrategy.com/openapi.json
- **API base URL:** `https://app.clearpointstrategy.com/api/v1`

## Authentication

### Header API Keys

Authenticate every request with the ClearPoint accessKey and secretKey headers.

### Credentials

- **Access Key:** `accessKey` · required · ClearPoint access key sent on every request as the accessKey header.

Send these headers with each API request:

```http
accessKey: <accessKey>
secretKey: <secretKey>
```

[Official authentication documentation](https://support.clearpointstrategy.com/en/articles/8650000-automation-integration-access-the-api-getting-and-using-clearpoint-api-keys)

## Pagination

Use `count` in the query string to set the page size (default 25; minimum 1). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Favorite](actions/check-favorite.md) | `GET /favorites` | [docs](https://developer.clearpointstrategy.com/reference/checkfavorite-2) |
| [Get Action Item](actions/get-action-item.md) | `GET /actionItems/{actionItemId}` | [docs](https://developer.clearpointstrategy.com/reference/getactionitem-2) |
| [Get Attachment](actions/get-attachment.md) | `GET /attachments/{attachmentId}` | [docs](https://developer.clearpointstrategy.com/reference/getattachment-2) |
| [Get File](actions/get-file.md) | `GET /files/{fileId}` | [docs](https://developer.clearpointstrategy.com/reference/getfile-2) |
| [Get Goal](actions/get-goal.md) | `GET /goals/{goalId}` | [docs](https://developer.clearpointstrategy.com/reference/getgoal-2) |
| [Get Group](actions/get-group.md) | `GET /groups/{groupId}` | [docs](https://developer.clearpointstrategy.com/reference/getgroup-2) |
| [Get Initiative](actions/get-initiative.md) | `GET /initiatives/{initiativeId}` | [docs](https://developer.clearpointstrategy.com/reference/getinitiative-2) |
| [Get Measure](actions/get-measure.md) | `GET /measures/{measureId}` | [docs](https://developer.clearpointstrategy.com/reference/getmeasure-2) |
| [Get Notification](actions/get-notification.md) | `GET /notifications/{notificationId}` | [docs](https://developer.clearpointstrategy.com/reference/getnotification-1) |
| [Get Objective](actions/get-objective.md) | `GET /objectives/{objectiveId}` | [docs](https://developer.clearpointstrategy.com/reference/getobjective-2) |
| [Get Report](actions/get-report.md) | `GET /reports/{reportId}` | [docs](https://developer.clearpointstrategy.com/reference/getreport-2) |
| [Get Risk](actions/get-risk.md) | `GET /risks/{riskId}` | [docs](https://developer.clearpointstrategy.com/reference/getrisk-2) |
| [Get Schedule](actions/get-schedule.md) | `GET /schedules/{scheduleId}` | [docs](https://developer.clearpointstrategy.com/reference/getschedule-2) |
| [Get Scorecard](actions/get-scorecard.md) | `GET /scorecards/{scorecardId}` | [docs](https://developer.clearpointstrategy.com/reference/getscorecard-2) |
| [Get User](actions/get-user.md) | `GET /users/{userId}` | [docs](https://developer.clearpointstrategy.com/reference/getuser-2) |
| [List Action Items](actions/list-action-items.md) | `GET /actionItems` | [docs](https://developer.clearpointstrategy.com/reference/listactionitems-2) |
| [List Attachments](actions/list-attachments.md) | `GET /attachments` | [docs](https://developer.clearpointstrategy.com/reference/listattachments-2) |
| [List Files](actions/list-files.md) | `GET /files` | [docs](https://developer.clearpointstrategy.com/reference/listfiles-2) |
| [List Goals](actions/list-goals.md) | `GET /goals` | [docs](https://developer.clearpointstrategy.com/reference/listgoals-2) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://developer.clearpointstrategy.com/reference/listgroups-2) |
| [List Initiatives](actions/list-initiatives.md) | `GET /initiatives` | [docs](https://developer.clearpointstrategy.com/reference/listinitiatives-2) |
| [List Measures](actions/list-measures.md) | `GET /measures` | [docs](https://developer.clearpointstrategy.com/reference/listmeasures-2) |
| [List Notifications](actions/list-notifications.md) | `GET /notifications` | [docs](https://developer.clearpointstrategy.com/reference/listadminnotifications-2) |
| [List Objectives](actions/list-objectives.md) | `GET /objectives` | [docs](https://developer.clearpointstrategy.com/reference/listobjectives-2) |
| [List Reports](actions/list-reports.md) | `GET /reports` | [docs](https://developer.clearpointstrategy.com/reference/listreports-2) |
| [List Risks](actions/list-risks.md) | `GET /risks` | [docs](https://developer.clearpointstrategy.com/reference/listrisks-2) |
| [List Schedules](actions/list-schedules.md) | `GET /schedules` | [docs](https://developer.clearpointstrategy.com/reference/listschedules-2) |
| [List Scorecards](actions/list-scorecards.md) | `GET /scorecards` | [docs](https://developer.clearpointstrategy.com/reference/listscorecards-2) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://developer.clearpointstrategy.com/reference/listusers-2) |
| [Search](actions/search.md) | `POST /search` | [docs](https://developer.clearpointstrategy.com/reference/search-5) |
