# Get Customer Conversation Preferences with mittwald

Retrieves customer conversation preferences from mittwald API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/customers/:customerId/conversation-preferences`
- **Base URL:** `https://api.mittwald.de`
- **Official documentation:** [Get Customer Conversation Preferences](https://api.mittwald.de/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | yes | The unique identifier of the customer. |
