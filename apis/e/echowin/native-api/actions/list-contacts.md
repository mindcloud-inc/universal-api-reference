# List Contacts with echowin

Retrieves contacts from echowin.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://echo.win/api/v1`
- **Official documentation:** [List Contacts](https://echo.win/api-docs/contacts#list-contacts)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search contacts by name, email, or phone number |
| `tagIds` | query | `string` | no | Filter by tag IDs as a comma-separated list |
