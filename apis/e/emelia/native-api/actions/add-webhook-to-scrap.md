# Add Webhook To Scrap with Emelia

Adds a webhook to a scrap in Emelia.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://graphql.emelia.io`
- **Official documentation:** [Add Webhook To Scrap](https://docs-old.emelia.io/#operation-add_webhook_to_a_scrap-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `events` | body | `string` | yes | Webhook event list. Provide a JSON array string, for example ["finished"]. |
| `id` | body | `string` | yes | Scrap identifier |
| `webhookUrl` | body | `string` | yes | Webhook URL |
