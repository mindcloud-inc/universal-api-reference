# Update Webhook with Clockify

Updates an existing webhook in Clockify.

## Endpoint

- **Method:** `PUT`
- **Path:** `workspaces/:workspaceId/webhooks/:webhookId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Update Webhook](https://docs.developer.clockify.me/#tag/Webhooks/operation/updateWebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | — |
| `webhookId` | path | `string<string>` | yes | — |
| `triggerSource[]` | body | `array<string>` | yes | — |
| `triggerSourceType` | body | `list<string>` | yes | Accepted values: `ASSIGNMENT_ID`, `EXPENSE_ID`, `PROJECT_ID`, `TAG_ID`, `TASK_ID`, `USER_ID`, `WORKSPACE_ID`. |
| `url` | body | `string` | yes | — |
| `webhookEvent` | body | `list<string>` | yes | Accepted values: `APPROVAL_REQUEST_STATUS_UPDATED`, `ASSIGNMENT_CREATED`, `ASSIGNMENT_DELETED`, `ASSIGNMENT_PUBLISHED`, `ASSIGNMENT_UPDATED`, `BALANCE_UPDATED`, `BILLABLE_RATE_UPDATED`, `CLIENT_DELETED`, `CLIENT_UPDATED`, `COST_RATE_UPDATED`, `EXPENSE_CREATED`, `EXPENSE_DELETED`, `EXPENSE_RESTORED`, `EXPENSE_UPDATED`, `INVOICE_UPDATED`, `LIMITED_USERS_ADDED_TO_WORKSPACE`, `NEW_APPROVAL_REQUEST`, `NEW_CLIENT`, `NEW_INVOICE`, `NEW_PROJECT`, `NEW_TAG`, `NEW_TASK`, `NEW_TIMER_STARTED`, `NEW_TIME_ENTRY`, `PROJECT_DELETED`, `PROJECT_UPDATED`, `TAG_DELETED`, `TAG_UPDATED`, `TASK_DELETED`, `TASK_UPDATED`, `TIMER_STOPPED`, `TIME_ENTRY_DELETED`, `TIME_ENTRY_RESTORED`, `TIME_ENTRY_SPLIT`, `TIME_ENTRY_UPDATED`, `TIME_OFF_REQUESTED`, `TIME_OFF_REQUEST_APPROVED`, `TIME_OFF_REQUEST_REJECTED`, `TIME_OFF_REQUEST_UPDATED`, `TIME_OFF_REQUEST_WITHDRAWN`, `USERS_INVITED_TO_WORKSPACE`, `USER_ACTIVATED_ON_WORKSPACE`, `USER_DEACTIVATED_ON_WORKSPACE`, `USER_DELETED_FROM_WORKSPACE`, `USER_EMAIL_CHANGED`, `USER_GROUP_CREATED`, `USER_GROUP_DELETED`, `USER_GROUP_UPDATED`, `USER_JOINED_WORKSPACE`, `USER_UPDATED`. |
| `name` | body | `string` | no | Maximum length: 30. |
