# Remove Webhook From Scrap with Emelia

Deletes a webhook from a scrap in Emelia.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://graphql.emelia.io`
- **Official documentation:** [Remove Webhook From Scrap](https://docs-old.emelia.io/#operation-remove_webhook_to_a_scrap-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Scrap identifier |
| `webhookUrl` | body | `string` | yes | Webhook URL |
