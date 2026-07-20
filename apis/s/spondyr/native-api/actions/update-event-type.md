# Update Event Type with Spondyr

Updates an existing event type for a transaction type in Spondyr.

## Endpoint

- **Method:** `PUT`
- **Path:** `/EventType`
- **Base URL:** `https://client.spondyr.io/api/v1.0.0/`
- **Official documentation:** [Update Event Type](https://client.spondyr.io/Public/Public/APIDocumentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `TransactionType` | body | `string` | yes | The transaction type the event type belongs to. |
| `EventType` | body | `string` | yes | The existing event type name to update. |
| `Name` | body | `string` | yes | The new event type name. |
