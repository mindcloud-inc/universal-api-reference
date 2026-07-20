# Retrieve Webhook with Polaria

Retrieves a webhook from Polaria.

## Endpoint

- **Method:** `GET`
- **Path:** `/widgets/[:api_key]/webhooks/[:id]`
- **Base URL:** `https://app.polaria.ai/rest/v2`
- **Official documentation:** [Retrieve Webhook](https://help.polaria.ai/hc/rest-api-webhooks/get-widgets-api_key-webhooks-id-retrieve-a-webhook-2?lang=en)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `api_key` | path | `string` | yes | The Polaria widget API key for the target brand. |
| `id` | path | `string` | yes | The ID of the webhook to retrieve. |
