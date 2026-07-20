# Update Webhook with Parsio

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://api.parsio.io`
- **Official documentation:** [Update Webhook](https://help.parsio.io/public-api/parsio-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `_id` | body | `string` | yes | Webhook ID. |
| `url` | body | `string` | no | Destination webhook URL. |
| `event` | body | `string` | no | Trigger event. |
| `enabled` | body | `boolean` | no | Whether the webhook is enabled. |
| `table_id` | body | `string` | no | Table ID for table.parsed events. |
