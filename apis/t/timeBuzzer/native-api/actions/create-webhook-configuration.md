# Create Webhook Configuration with timeBuzzer

## Endpoint

- **Method:** `POST`
- **Path:** `/open-api/webhooks`
- **Base URL:** `https://my.timebuzzer.com`
- **Official documentation:** [Create Webhook Configuration](https://my.timebuzzer.com/doc/#api-Webhook-SaveNewWebhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The webhook target URL. |
| `event` | body | `string` | yes | The webhook event name. |
| `active` | body | `boolean` | yes | Whether the webhook is active. |
