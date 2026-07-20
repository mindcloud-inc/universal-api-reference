# Delete Organization Webhook with Zeplin

Deletes an existing organization webhook from Zeplin.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/organizations/{organization_id}/webhooks/{webhook_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Delete Organization Webhook](https://docs.zeplin.dev/reference/deleteorganizationwebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | path | `string` | yes | Organization id |
| `webhook_id` | path | `string` | yes | Webhook id |
