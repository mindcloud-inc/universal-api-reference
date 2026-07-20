# SafetyCulture: Native API Reference

A consolidated summary of SafetyCulture's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://developer.safetyculture.com/reference
- **API base URL:** `https://api.safetyculture.io`

## Authentication

### API Token

Authenticate with a SafetyCulture API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.safetyculture.com/reference/introduction)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Comment to Issue Timeline](actions/add-comment-to-issue-timeline.md) | `POST /tasks/v1/timeline/comments` | [docs](https://developer.safetyculture.com/reference/timelineservice_addcomment) |
| [Complete Inspection](actions/complete-inspection.md) | `POST /inspections/integration/v1/inspections/{inspection_id}/complete` | [docs](https://developer.safetyculture.com/reference/inspectionservice_completeinspection) |
| [Create Action](actions/create-action.md) | `POST /tasks/v1/actions` | [docs](https://developer.safetyculture.com/reference/actionsservice_createaction) |
| [Create Issue](actions/create-issue.md) | `POST /tasks/v1/incidents/submit` | [docs](https://developer.safetyculture.com/reference/incidentsservice_submitincident) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks/v1/webhooks` | [docs](https://developer.safetyculture.com/reference/webhooksservice_createwebhook) |
| [Generate Inspection Deep Link](actions/generate-inspection-deep-link.md) | `POST /audits/{audit_id}/deep_link` | [docs](https://developer.safetyculture.com/reference/thepubservice_getinspectiondeeplink) |
| [Get Action](actions/get-action.md) | `GET /tasks/v1/actions/{id}` | [docs](https://developer.safetyculture.com/reference/actionsservice_getaction) |
| [Get Inspection](actions/get-inspection.md) | `GET /inspections/v1/inspections/{id}` | [docs](https://developer.safetyculture.com/reference/inspectionservice_getinspection) |
| [Get Inspection Answers](actions/get-inspection-answers.md) | `GET /inspections/v1/answers/{id}` | [docs](https://developer.safetyculture.com/reference/answerservice_getanswersforinspection) |
| [Get Inspection Details](actions/get-inspection-details.md) | `GET /inspections/v1/inspections/{id}/details` | [docs](https://developer.safetyculture.com/reference/externalinspectionservice_getinspectiondetails) |
| [Get Inspection Web Report Link](actions/get-inspection-web-report-link.md) | `GET /audits/{audit_id}/web_report_link` | [docs](https://developer.safetyculture.com/reference/thepubservice_getinspectionwebreportlink) |
| [Get Issue](actions/get-issue.md) | `GET /tasks/v1/incident/{id}` | [docs](https://developer.safetyculture.com/reference/incidentsservice_getincidentbyid) |
| [Get Template](actions/get-template.md) | `GET /templates/v1/templates/{template_id}` | [docs](https://developer.safetyculture.com/reference/templatesservice_gettemplatebyid) |
| [Get Template by Inspection](actions/get-template-by-inspection.md) | `GET /templates/v1/templates/inspections/{inspection_id}` | [docs](https://developer.safetyculture.com/reference/templatesservice_gettemplatebyinspectionid) |
| [List Actions](actions/list-actions.md) | `POST /tasks/v1/actions/list` | [docs](https://developer.safetyculture.com/reference/actionsservice_getactions) |
| [List Groups and Organizations](actions/list-groups-and-organizations.md) | `GET /share/connections` | [docs](https://developer.safetyculture.com/reference/thepubservice_getusergroups) |
| [List Issues](actions/list-issues.md) | `POST /tasks/v1/incidents/list` | [docs](https://developer.safetyculture.com/reference/incidentsservice_getincidents) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks/v1/webhooks` | [docs](https://developer.safetyculture.com/reference/webhooksservice_listwebhooks) |
| [Retrieve Selected Media](actions/retrieve-selected-media.md) | `GET /audits/{audit_id}/media/{media_id}` | [docs](https://developer.safetyculture.com/reference/thepubservice_getinspectionmedia) |
| [Search Modified Inspections](actions/search-modified-inspections.md) | `GET /audits/search` | [docs](https://developer.safetyculture.com/reference/thepubservice_searchinspections) |
| [Search Modified Templates](actions/search-modified-templates.md) | `GET /templates/search` | [docs](https://developer.safetyculture.com/reference/thepubservice_searchtemplates) |
| [Set Inspection Owner](actions/set-inspection-owner.md) | `PUT /inspections/v1/inspections/{inspection_id}/owner` | [docs](https://developer.safetyculture.com/reference/inspectionservice_setowner) |
| [Set Inspection Site](actions/set-inspection-site.md) | `PUT /inspections/v1/inspections/{inspection_id}/site` | [docs](https://developer.safetyculture.com/reference/inspectionservice_setinspectionsite) |
| [Start Inspection](actions/start-inspection.md) | `POST /audits` | [docs](https://developer.safetyculture.com/reference/thepubservice_startinspection) |
| [Update Action Assignees](actions/update-action-assignees.md) | `PUT /tasks/v1/actions/{task_id}/assignees` | [docs](https://developer.safetyculture.com/reference/actionsservice_updateassignees) |
| [Update Action Due Date](actions/update-action-due-date.md) | `PUT /tasks/v1/actions/{task_id}/due_at` | [docs](https://developer.safetyculture.com/reference/actionsservice_updatedueat) |
| [Update Action Priority](actions/update-action-priority.md) | `PUT /tasks/v1/actions/{task_id}/priority` | [docs](https://developer.safetyculture.com/reference/actionsservice_updatepriority) |
| [Update Action Status](actions/update-action-status.md) | `PUT /tasks/v1/actions/{task_id}/status` | [docs](https://developer.safetyculture.com/reference/actionsservice_updatestatus) |
| [Update Inspection](actions/update-inspection.md) | `PUT /audits/{audit_id}` | [docs](https://developer.safetyculture.com/reference/thepubservice_updateinspection) |
| [Update Issue Status](actions/update-issue-status.md) | `PUT /tasks/v1/incidents/{task_id}/status` | [docs](https://developer.safetyculture.com/reference/incidentsservice_updatestatus) |
