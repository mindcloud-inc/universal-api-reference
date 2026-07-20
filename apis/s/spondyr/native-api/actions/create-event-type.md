# Create Event Type with Spondyr

Creates a new event type for a transaction type in Spondyr.

## Endpoint

- **Method:** `POST`
- **Path:** `/EventType`
- **Base URL:** `https://client.spondyr.io/api/v1.0.0/`
- **Official documentation:** [Create Event Type](https://client.spondyr.io/Public/Public/APIDocumentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `TransactionType` | body | `string` | yes | The transaction type the event type belongs to. |
| `Name` | body | `string` | yes | The new event type name. |
