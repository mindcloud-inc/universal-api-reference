# Create Webhook with Parsio

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/:mailbox_id`
- **Base URL:** `https://api.parsio.io`
- **Official documentation:** [Create Webhook](https://help.parsio.io/public-api/parsio-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mailbox_id` | path | `string` | yes | Parsio mailbox ID. |
| `url` | body | `string` | yes | Destination webhook URL. |
| `event` | body | `string` | yes | Trigger event. |
| `enabled` | body | `boolean` | no | Whether the webhook is enabled. |
| `table_id` | body | `string` | no | Table ID for table.parsed events. |
