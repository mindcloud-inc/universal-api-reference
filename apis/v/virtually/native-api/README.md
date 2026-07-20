# Virtually: Native API Reference

A consolidated summary of Virtually's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://app.tryvirtually.com/api/docs
- **API base URL:** `https://app.tryvirtually.com`

## Authentication

### API Key

Authenticate with a personal Virtually API key.

### Credentials

- **API Key:** `apiKey` · required
- **Organization ID:** `orgId` · required · Your Virtually organization slug or ID, such as the workspace identifier used in the API path.

Send these headers with each API request:

```http
x-virtually-api-key: <apiKey>
```

[Official authentication documentation](https://intercom.help/virtually/en/articles/6613473-virtually-onboarding-guide)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Action](actions/create-action.md) | `POST /api/v2/orgs/:orgId/actions` | [docs](https://app.tryvirtually.com/api/docs#/Actions/ActionsController_create) |
| [Create Automation](actions/create-automation.md) | `POST /api/v2/orgs/:orgId/automations` | [docs](https://app.tryvirtually.com/api/docs#/Automations/AutomationsController_create) |
| [Create Custom Data Record](actions/create-custom-data-record.md) | `POST /api/v2/orgs/:orgId/customData` | [docs](https://app.tryvirtually.com/api/docs#/Custom%20Data/CustomDataController_create) |
| [Create Member](actions/create-member.md) | `POST /api/v2/orgs/:orgId/members` | [docs](https://app.tryvirtually.com/api/docs#/Members/MembersController_create) |
| [Create Trigger](actions/create-trigger.md) | `POST /api/v2/orgs/:orgId/triggers` | [docs](https://app.tryvirtually.com/api/docs#/Triggers/TriggersController_create) |
| [Delete Action](actions/delete-action.md) | `DELETE /api/v2/orgs/:orgId/actions/:actionId` | [docs](https://app.tryvirtually.com/api/docs#/Actions/ActionsController_remove) |
| [Delete Automation](actions/delete-automation.md) | `DELETE /api/v2/orgs/:orgId/automations/:id` | [docs](https://app.tryvirtually.com/api/docs#/Automations/AutomationsController_remove) |
| [Delete Member](actions/delete-member.md) | `DELETE /api/v2/orgs/:orgId/members/:memberId` | [docs](https://app.tryvirtually.com/api/docs#/Members/MembersController_remove) |
| [Delete Trigger](actions/delete-trigger.md) | `DELETE /api/v2/orgs/:orgId/triggers/:triggerId` | [docs](https://app.tryvirtually.com/api/docs#/Triggers/TriggersController_remove) |
| [Get Action](actions/get-action.md) | `GET /api/v2/orgs/:orgId/actions/:id` | [docs](https://app.tryvirtually.com/api/docs#/Actions/ActionsController_findOne) |
| [Get Automation](actions/get-automation.md) | `GET /api/v2/orgs/:orgId/automations/:id` | [docs](https://app.tryvirtually.com/api/docs#/Automations/AutomationsController_findOne) |
| [Get Member](actions/get-member.md) | `GET /api/v2/orgs/:orgId/members/:memberId` | [docs](https://app.tryvirtually.com/api/docs#/Members/MembersController_findOne) |
| [Get Member Attendance](actions/get-member-attendance.md) | `GET /api/v2/orgs/:orgId/members/:memberId/attendance` | [docs](https://app.tryvirtually.com/api/docs#/Members/MembersController_getMemberAttendance) |
| [Get Organization](actions/get-organization.md) | `GET /api/v2/orgs/:orgId` | [docs](https://app.tryvirtually.com/api/docs#/App/AppController_getOrg) |
| [Get Report Summary](actions/get-report-summary.md) | `GET /api/v2/orgs/:orgId/reports/summary` | [docs](https://app.tryvirtually.com/api/docs#/Reports/ReportsController_getSummary) |
| [Get Trigger](actions/get-trigger.md) | `GET /api/v2/orgs/:orgId/triggers/:triggerId` | [docs](https://app.tryvirtually.com/api/docs#/Triggers/TriggersController_findOne) |
| [List Actions](actions/list-actions.md) | `GET /api/v2/orgs/:orgId/actions` | [docs](https://app.tryvirtually.com/api/docs#/Actions/ActionsController_findAll) |
| [List Activity Feed Entries](actions/list-activity-feed-entries.md) | `GET /api/v2/orgs/:orgId/activity-feed` | [docs](https://app.tryvirtually.com/api/docs#/App/AppController_getActivityLogs) |
| [List Automations](actions/list-automations.md) | `GET /api/v2/orgs/:orgId/automations` | [docs](https://app.tryvirtually.com/api/docs#/Automations/AutomationsController_findAll) |
| [List Custom Data Keys](actions/list-custom-data-keys.md) | `GET /api/v2/orgs/:orgId/customData/keys` | [docs](https://app.tryvirtually.com/api/docs#/Custom%20Data/CustomDataController_getOrgCustomDataEventKeys) |
| [List Custom Data Records](actions/list-custom-data-records.md) | `GET /api/v2/orgs/:orgId/customData` | [docs](https://app.tryvirtually.com/api/docs#/Custom%20Data/CustomDataController_findAll) |
| [List Member Tags](actions/list-member-tags.md) | `GET /api/v2/orgs/:orgId/members/tags` | [docs](https://app.tryvirtually.com/api/docs#/Members/MembersController_getTags) |
| [List Members](actions/list-members.md) | `GET /api/v2/orgs/:orgId/members` | [docs](https://app.tryvirtually.com/api/docs#/Members/MembersController_findAll) |
| [List Reports](actions/list-reports.md) | `GET /api/v2/orgs/:orgId/reports` | [docs](https://app.tryvirtually.com/api/docs#/Reports/ReportsController_findAll) |
| [List Sender Profiles](actions/list-sender-profiles.md) | `GET /api/v2/orgs/:orgId/members/senderProfiles/:platformName` | [docs](https://app.tryvirtually.com/api/docs#/Members/MembersController_getSenderProfiles) |
| [List Triggers](actions/list-triggers.md) | `GET /api/v2/orgs/:orgId/triggers` | [docs](https://app.tryvirtually.com/api/docs#/Triggers/TriggersController_findAll) |
| [Update Action](actions/update-action.md) | `PATCH /api/v2/orgs/:orgId/actions/:actionId` | [docs](https://app.tryvirtually.com/api/docs#/Actions/ActionsController_update) |
| [Update Automation](actions/update-automation.md) | `PATCH /api/v2/orgs/:orgId/automations/:id` | [docs](https://app.tryvirtually.com/api/docs#/Automations/AutomationsController_update) |
| [Update Member](actions/update-member.md) | `PATCH /api/v2/orgs/:orgId/members/:memberId` | [docs](https://app.tryvirtually.com/api/docs#/Members/MembersController_update) |
| [Update Trigger](actions/update-trigger.md) | `PATCH /api/v2/orgs/:orgId/triggers/:triggerId` | [docs](https://app.tryvirtually.com/api/docs#/Triggers/TriggersController_update) |
| [Upsert Tags](actions/upsert-tags.md) | `PUT /api/v2/orgs/:orgId/tags` | [docs](https://app.tryvirtually.com/api/docs#/Tags/TagsController_create) |
