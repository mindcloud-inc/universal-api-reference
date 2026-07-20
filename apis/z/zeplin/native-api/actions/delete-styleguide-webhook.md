# Delete Styleguide Webhook with Zeplin

Deletes an existing styleguide webhook from Zeplin.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/styleguides/{styleguide_id}/webhooks/{webhook_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Delete Styleguide Webhook](https://docs.zeplin.dev/reference/deletestyleguidewebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `styleguide_id` | path | `string` | yes | Styleguide id |
| `webhook_id` | path | `string` | yes | Webhook id |
