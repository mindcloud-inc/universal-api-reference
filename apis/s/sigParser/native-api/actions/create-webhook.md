# Create Webhook with SigParser

## Endpoint

- **Method:** `POST`
- **Path:** `/api/Webhooks`
- **Base URL:** `https://ipaas.sigparser.com`
- **Official documentation:** [Create Webhook](https://ipaas.sigparser.com/v1#post-api-webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The webhook URL to post events to. |
| `action` | body | `string` | yes | Webhook event type, such as contact.createorupdate or company.createorupdate. |
| `batch_frequency_cron_expression` | body | `string` | no | Cron frequency for batching webhook delivery. |
