# List Event Types with Spondyr

Retrieves event types for a transaction type in Spondyr.

## Endpoint

- **Method:** `GET`
- **Path:** `/EventTypes`
- **Base URL:** `https://client.spondyr.io/api/v1.0.0/`
- **Official documentation:** [List Event Types](https://client.spondyr.io/Public/Public/APIDocumentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `TransactionType` | query | `string` | no | Optional transaction type filter. |
