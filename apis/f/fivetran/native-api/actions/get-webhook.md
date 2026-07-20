# Get Webhook with Fivetran

Retrieves a webhook from your Fivetran account.

## Endpoint

- **Method:** `GET`
- **Path:** `/webhooks/[:webhookId]`
- **Base URL:** `https://api.fivetran.com/v1`
- **Official documentation:** [Get Webhook](https://fivetran.com/docs/rest-api/api-reference/webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhookId` | path | `string` | yes | The Fivetran webhook ID. |
