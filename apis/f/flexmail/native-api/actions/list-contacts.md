# List Contacts with Flexmail

Retrieves contact records from your Flexmail account.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://api.flexmail.eu`
- **Official documentation:** [List Contacts](https://api.flexmail.eu/documentation/#get-/contacts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | An email address to filter on. |
