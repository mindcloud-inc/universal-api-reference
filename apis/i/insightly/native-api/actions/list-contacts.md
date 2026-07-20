# List Contacts with Insightly

Retrieves a list of contacts from Insightly.

## Endpoint

- **Method:** `GET`
- **Path:** `{apiBaseUrl}Contacts`
- **Base URL:** `https://api.na1.insightly.com/v3.1/`
- **Official documentation:** [List Contacts](https://api.insightly.com/v3.1/Help#!/Contacts/GetEntities)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `brief` | query | `boolean` | no | Return only top-level properties for each contact. |
| `count_total` | query | `boolean` | no | Return the total-record count in the response headers. |
