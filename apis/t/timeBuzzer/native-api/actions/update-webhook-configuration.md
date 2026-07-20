# Update Webhook Configuration with timeBuzzer

## Endpoint

- **Method:** `PUT`
- **Path:** `/open-api/webhooks/:id`
- **Base URL:** `https://my.timebuzzer.com`
- **Official documentation:** [Update Webhook Configuration](https://my.timebuzzer.com/doc/#api-Webhook-SaveWebhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The webhook ID. |
| `url` | body | `string` | yes | The webhook target URL. |
| `event` | body | `string` | yes | The webhook event name. |
| `active` | body | `boolean` | yes | Whether the webhook is active. |
