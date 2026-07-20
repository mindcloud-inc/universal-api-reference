# Get Customer AI Hosting Key with mittwald

Retrieves a customer AI hosting key from mittwald API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/customers/:customerId/ai-hosting-keys/:keyId`
- **Base URL:** `https://api.mittwald.de`
- **Official documentation:** [Get Customer AI Hosting Key](https://api.mittwald.de/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | yes | Customer ID |
| `keyId` | path | `string` | yes | Key ID |
