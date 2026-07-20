# Get Condition with Spondyr

Retrieves a condition for a transaction type in Spondyr.

## Endpoint

- **Method:** `GET`
- **Path:** `/Condition`
- **Base URL:** `https://client.spondyr.io/api/v1.0.0/`
- **Official documentation:** [Get Condition](https://client.spondyr.io/Public/Public/APIDocumentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `TransactionType` | query | `string` | no | Optional transaction type context. |
| `Condition` | query | `string` | yes | The condition name to retrieve. |
