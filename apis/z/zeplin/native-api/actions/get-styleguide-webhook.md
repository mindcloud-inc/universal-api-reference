# Get Styleguide Webhook with Zeplin

Retrieves a styleguide webhook from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/styleguides/{styleguide_id}/webhooks/{webhook_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Get Styleguide Webhook](https://docs.zeplin.dev/reference/getstyleguidewebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `styleguide_id` | path | `string` | yes | Styleguide id |
| `webhook_id` | path | `string` | yes | Webhook id |
