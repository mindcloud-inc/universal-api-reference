# Create Webhook with Polaria

Creates a new webhook in Polaria.

## Endpoint

- **Method:** `POST`
- **Path:** `/widgets/[:api_key]/webhooks`
- **Base URL:** `https://app.polaria.ai/rest/v2`
- **Official documentation:** [Create Webhook](https://help.polaria.ai/hc/rest-api-webhooks/post-widgets-api_key-webhooks-id-create-a-webhook-2?lang=en)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `api_key` | path | `string` | yes | The Polaria widget API key for the target brand. |
| `event` | body | `string` | yes | — |
| `url` | body | `string` | yes | — |
