# <img src="https://images.mindcloud.co/apps/icons/shuffler_1775750718406.png" alt="Shuffler logo" width="28" height="28"> Shuffler: Universal API

Official Shuffle API integration for workflows, executions, datastore, files, notifications, organizations, schedules, hooks, apps, and authentication management.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/shuffler/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 56
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://shuffler.io
- **Vendor API docs:** https://shuffler.io/docs/API

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Apps](actions/list-apps.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/list-apps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (56)

### API Keys

| Action | Method | Description |
| --- | --- | --- |
| [Generate API Key](actions/generate-api-key.md) | POST | Creates an API key in Shuffler. |

### Applications

| Action | Method | Description |
| --- | --- | --- |
| [List Apps](actions/list-apps.md) | GET | Retrieves apps from Shuffler. |
| [Search Apps](actions/search-apps.md) | GET | Finds apps in Shuffler by search query. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [List Active Categories](actions/list-active-categories.md) | GET | Retrieves active categories from Shuffler. |
| [Run Category Action](actions/run-category-action.md) | POST | Creates a category action run in Shuffler. |

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [Configure App Authentication](actions/configure-app-authentication.md) | PUT | Updates an app authentication in Shuffler. |
| [Create App Authentication](actions/create-app-authentication.md) | POST | Creates an app authentication in Shuffler. |
| [Delete App Authentication](actions/delete-app-authentication.md) | DELETE | Deletes an app authentication from Shuffler. |
| [List App Authentications](actions/list-app-authentications.md) | GET | Retrieves app authentications from Shuffler. |

### Environments

| Action | Method | Description |
| --- | --- | --- |
| [List Environments](actions/list-environments.md) | GET | Retrieves environments from Shuffler. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Create File](actions/create-file.md) | POST | Creates a file in Shuffler. |
| [Delete File](actions/delete-file.md) | DELETE | Deletes a file from Shuffler. |
| [Download File](actions/download-file.md) | GET | Retrieves file content from Shuffler. |
| [Edit File](actions/edit-file.md) | PUT | Updates an existing file in Shuffler. |
| [Get File Metadata](actions/get-file-metadata.md) | GET | Retrieves file metadata from Shuffler. |
| [List Files](actions/list-files.md) | GET | Retrieves files from Shuffler. |
| [List Files in Namespace](actions/list-files-in-namespace.md) | GET | Retrieves files in a Shuffler namespace. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Set Datastore Keys](actions/bulk-set-datastore-keys.md) | POST | Creates multiple datastore keys in Shuffler. |
| [Delete Datastore Key](actions/delete-datastore-key.md) | DELETE | Deletes a datastore key from Shuffler. |
| [Get Datastore Key](actions/get-datastore-key.md) | GET | Retrieves a datastore key from Shuffler. |
| [List Datastore Keys](actions/list-datastore-keys.md) | GET | Retrieves datastore keys from Shuffler. |
| [Set Datastore Key](actions/set-datastore-key.md) | POST | Creates a datastore key in Shuffler. |

### Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Increment Custom Stat](actions/increment-custom-stat.md) | POST | Increments a custom stat in Shuffler. |

### Notifications

| Action | Method | Description |
| --- | --- | --- |
| [Clear Notifications](actions/clear-notifications.md) | PUT | Marks all notifications as read in Shuffler. |
| [Create Notification](actions/create-notification.md) | POST | Creates a notification in Shuffler. |
| [List Notifications](actions/list-notifications.md) | GET | Retrieves notifications from Shuffler. |
| [Mark Notification Read](actions/mark-notification-read.md) | PUT | Marks a notification as read in Shuffler. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Change Current Organization](actions/change-current-organization.md) | PUT | Updates the current organization in Shuffler. |
| [Create Suborganization](actions/create-suborganization.md) | POST | Creates a suborganization in Shuffler. |
| [Delete Organization](actions/delete-organization.md) | DELETE | Deletes an existing organization from Shuffler. |
| [Generate SSO Login Link](actions/generate-sso-login-link.md) | POST | Creates an SSO login link in Shuffler. |
| [Get Organization](actions/get-organization.md) | GET | Retrieves an organization from Shuffler. |
| [Invite User to Organization](actions/invite-user-to-organization.md) | POST | Creates an organization invitation in Shuffler. |
| [List Child Organizations](actions/list-child-organizations.md) | GET | Retrieves child organizations from Shuffler. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from Shuffler. |
| [Update Organization](actions/update-organization.md) | PUT | Updates an existing organization in Shuffler. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Stats](actions/get-organization-stats.md) | GET | Retrieves organization stats from Shuffler. |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [Delete Workflow Schedule](actions/delete-workflow-schedule.md) | DELETE | Deletes a workflow schedule from Shuffler. |
| [List Workflow Schedules](actions/list-workflow-schedules.md) | GET | Retrieves workflow schedules from Shuffler. |
| [Schedule Workflow](actions/schedule-workflow.md) | POST | Creates a workflow schedule in Shuffler. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Delete User](actions/delete-user.md) | DELETE | Deactivates an existing user in Shuffler. |
| [Get Users](actions/get-users.md) | GET | Retrieves users from Shuffler. |
| [Register User](actions/register-user.md) | POST | Creates a user in Shuffler. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in Shuffler. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a webhook in Shuffler. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook from Shuffler. |

### Workflow Runs

| Action | Method | Description |
| --- | --- | --- |
| [Abort Workflow Execution](actions/abort-workflow-execution.md) | PUT | Aborts a workflow execution in Shuffler. |
| [Execute Workflow](actions/execute-workflow.md) | POST | Creates a workflow execution in Shuffler. |
| [Get Execution Results](actions/get-execution-results.md) | GET | Retrieves execution results from Shuffler. |
| [List Workflow Executions](actions/list-workflow-executions.md) | GET | Retrieves workflow executions from Shuffler. |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [Create Workflow](actions/create-workflow.md) | POST | Creates a new workflow in Shuffler. |
| [Delete Workflow](actions/delete-workflow.md) | DELETE | Deletes an existing workflow from Shuffler. |
| [Get Workflow](actions/get-workflow.md) | GET | Retrieves a workflow from Shuffler. |
| [List Workflows](actions/list-workflows.md) | GET | Retrieves workflows from Shuffler. |
| [Update Workflow](actions/update-workflow.md) | PUT | Updates an existing workflow in Shuffler. |
| [Upload Remote Workflows](actions/upload-remote-workflows.md) | POST | Uploads remote workflows to Shuffler. |

