# Shuffler: Native API Reference

A consolidated summary of Shuffler's API configuration and 56 documented operations, with links to official documentation.

- **Official docs:** https://shuffler.io/docs/API
- **API base URL:** `https://shuffler.io/api/v1`

## Authentication

### API Key

Authenticate with a Shuffle API key sent as Authorization: Bearer <APIKEY>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://shuffler.io/docs/API)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (56 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Abort Workflow Execution](actions/abort-workflow-execution.md) | `GET /workflows/{workflowId}/executions/{executionId}/abort` | [docs](https://shuffler.io/docs/API#abort-workflow) |
| [Bulk Set Datastore Keys](actions/bulk-set-datastore-keys.md) | `POST /v2/datastore` | [docs](https://shuffler.io/docs/API#add-multiple-keys) |
| [Change Current Organization](actions/change-current-organization.md) | `POST /orgs/{orgId}/change` | [docs](https://shuffler.io/docs/API#change-current-organization) |
| [Clear Notifications](actions/clear-notifications.md) | `GET /notifications/clear` | [docs](https://shuffler.io/docs/API#mark-all-notifications-as-read) |
| [Configure App Authentication](actions/configure-app-authentication.md) | `POST /apps/authentication/{authenticationId}/config` | [docs](https://shuffler.io/docs/API#set-authentication-everywhere) |
| [Create App Authentication](actions/create-app-authentication.md) | `PUT /apps/authentication` | [docs](https://shuffler.io/docs/API#add-app-authentication) |
| [Create File](actions/create-file.md) | `POST /files/create` | [docs](https://shuffler.io/docs/API#create-a-file) |
| [Create Notification](actions/create-notification.md) | `POST /notifications` | [docs](https://shuffler.io/docs/API#create-a-notification) |
| [Create Suborganization](actions/create-suborganization.md) | `POST /orgs/{orgId}/create_sub_org` | [docs](https://shuffler.io/docs/API#create-a-suborg) |
| [Create Webhook](actions/create-webhook.md) | `POST /hooks` | [docs](https://shuffler.io/docs/API#create-and-start-webhook) |
| [Create Workflow](actions/create-workflow.md) | `POST /workflows` | [docs](https://shuffler.io/docs/API#create-new-workflow) |
| [Delete App Authentication](actions/delete-app-authentication.md) | `DELETE /apps/authentication/{authenticationId}` | [docs](https://shuffler.io/docs/API#delete-app-authentication) |
| [Delete Datastore Key](actions/delete-datastore-key.md) | `POST /orgs/{orgId}/delete_cache` | [docs](https://shuffler.io/docs/API#delete-a-key) |
| [Delete File](actions/delete-file.md) | `DELETE /files/{fileId}` | [docs](https://shuffler.io/docs/API#delete-a-file) |
| [Delete Organization](actions/delete-organization.md) | `DELETE /orgs/{orgId}` | [docs](https://shuffler.io/docs/API#delete-organizations) |
| [Delete User](actions/delete-user.md) | `DELETE /users/{userId}` | [docs](https://shuffler.io/docs/API#deactivates-a-user) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /hooks/{webhookId}` | [docs](https://shuffler.io/docs/API#delete-and-stop-webhook) |
| [Delete Workflow](actions/delete-workflow.md) | `DELETE /workflows/{workflowId}` | [docs](https://shuffler.io/docs/API#delete-a-workflow) |
| [Delete Workflow Schedule](actions/delete-workflow-schedule.md) | `DELETE /workflows/{workflowId}/schedule/{scheduleId}` | [docs](https://shuffler.io/docs/API#stop-a-workflow-schedule) |
| [Download File](actions/download-file.md) | `GET /files/{fileId}/content` | [docs](https://shuffler.io/docs/API#download-a-file) |
| [Edit File](actions/edit-file.md) | `PUT /files/{fileId}/edit` | [docs](https://shuffler.io/docs/API#edit-an-existing-file) |
| [Execute Workflow](actions/execute-workflow.md) | `POST /workflows/{workflowId}/execute` | [docs](https://shuffler.io/docs/API#execute-workflow) |
| [Generate API Key](actions/generate-api-key.md) | `POST /users/generateapikey` | [docs](https://shuffler.io/docs/API#get-new-apikey) |
| [Generate SSO Login Link](actions/generate-sso-login-link.md) | `POST /orgs/sso/link` | [docs](https://shuffler.io/docs/API#generate-sso-login-link) |
| [Get Datastore Key](actions/get-datastore-key.md) | `POST /orgs/{orgId}/get_cache` | [docs](https://shuffler.io/docs/API#get-a-key) |
| [Get Execution Results](actions/get-execution-results.md) | `POST /streams/results` | [docs](https://shuffler.io/docs/API#get-execution-results) |
| [Get File Metadata](actions/get-file-metadata.md) | `POST /files/{fileId}` | [docs](https://shuffler.io/docs/API#get-file-meta-data) |
| [Get Organization](actions/get-organization.md) | `GET /orgs/{orgId}` | [docs](https://shuffler.io/docs/API#get-an-organization) |
| [Get Organization Stats](actions/get-organization-stats.md) | `GET /orgs/{orgId}/stats` | [docs](https://shuffler.io/docs/API#get-stats) |
| [Get Users](actions/get-users.md) | `GET /users/getusers` | [docs](https://shuffler.io/docs/API#list-users) |
| [Get Workflow](actions/get-workflow.md) | `GET /workflows/{workflowId}` | [docs](https://shuffler.io/docs/API#get-a-workflow) |
| [Increment Custom Stat](actions/increment-custom-stat.md) | `POST /orgs/{orgId}/stats` | [docs](https://shuffler.io/docs/API#count-stats-for-custom-key) |
| [Invite User to Organization](actions/invite-user-to-organization.md) | `POST /register_org` | [docs](https://shuffler.io/docs/API#invite-user-to-organization) |
| [List Active Categories](actions/list-active-categories.md) | `GET /apps/categories` | [docs](https://shuffler.io/docs/API#get-active-categories) |
| [List App Authentications](actions/list-app-authentications.md) | `GET /apps/authentication` | [docs](https://shuffler.io/docs/API#list-app-authentication) |
| [List Apps](actions/list-apps.md) | `GET /apps` | [docs](https://shuffler.io/docs/API#get-apps) |
| [List Child Organizations](actions/list-child-organizations.md) | `GET /orgs/{parentOrgId}/suborgs` | [docs](https://shuffler.io/docs/API#list-child-organizations) |
| [List Datastore Keys](actions/list-datastore-keys.md) | `GET /orgs/{orgId}/list_cache` | [docs](https://shuffler.io/docs/API#list-all-keys) |
| [List Environments](actions/list-environments.md) | `GET /getenvironments` | [docs](https://shuffler.io/docs/API#get-environments) |
| [List Files](actions/list-files.md) | `GET /files` | [docs](https://shuffler.io/docs/API#list-files) |
| [List Files in Namespace](actions/list-files-in-namespace.md) | `GET /files/namespaces/{category}` | [docs](https://shuffler.io/docs/API#get-file-category) |
| [List Notifications](actions/list-notifications.md) | `GET /notifications` | [docs](https://shuffler.io/docs/API#get-all-notifications) |
| [List Organizations](actions/list-organizations.md) | `GET /orgs` | [docs](https://shuffler.io/docs/API#list-organizations) |
| [List Workflow Executions](actions/list-workflow-executions.md) | `GET /workflows/{workflowId}/executions` | [docs](https://shuffler.io/docs/API#list-workflow-runs) |
| [List Workflow Schedules](actions/list-workflow-schedules.md) | `GET /workflows/schedules` | [docs](https://shuffler.io/docs/API#get-all-schedules) |
| [List Workflows](actions/list-workflows.md) | `GET /workflows` | [docs](https://shuffler.io/docs/API#list-all-workflows) |
| [Mark Notification Read](actions/mark-notification-read.md) | `GET /notifications/{notificationId}/markasread` | [docs](https://shuffler.io/docs/API#mark-notification-as-read) |
| [Register User](actions/register-user.md) | `POST /users/register` | [docs](https://shuffler.io/docs/API#register-a-new-user) |
| [Run Category Action](actions/run-category-action.md) | `POST /apps/categories/run` | [docs](https://shuffler.io/docs/API#shufflepy) |
| [Schedule Workflow](actions/schedule-workflow.md) | `POST /workflows/{workflowId}/schedule` | [docs](https://shuffler.io/docs/API#schedule-a-workflow) |
| [Search Apps](actions/search-apps.md) | `POST /apps/search` | [docs](https://shuffler.io/docs/API#search-existing-apps) |
| [Set Datastore Key](actions/set-datastore-key.md) | `POST /orgs/{orgId}/set_cache` | [docs](https://shuffler.io/docs/API#add-a-key) |
| [Update Organization](actions/update-organization.md) | `POST /orgs/{orgId}` | [docs](https://shuffler.io/docs/API#edit-organization) |
| [Update User](actions/update-user.md) | `PUT /users/updateuser` | [docs](https://shuffler.io/docs/API#update-a-user) |
| [Update Workflow](actions/update-workflow.md) | `PUT /workflows/{workflowId}` | [docs](https://shuffler.io/docs/API#save-a-workflow) |
| [Upload Remote Workflows](actions/upload-remote-workflows.md) | `POST /workflows/download_remote` | [docs](https://shuffler.io/docs/API#upload-a-workflow) |
