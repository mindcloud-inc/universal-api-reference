# Get Organization Webhook with Zeplin

Retrieves an organization webhook from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/{organization_id}/webhooks/{webhook_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Get Organization Webhook](https://docs.zeplin.dev/reference/getorganizationwebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | path | `string` | yes | Organization id |
| `webhook_id` | path | `string` | yes | Webhook id |
