# List Contacts with Nutshell

Retrieves contacts from Nutshell.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://app.nutshell.com/rest`
- **Official documentation:** [List Contacts](https://developers.nutshell.com/reference)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Search across contacts. |
| `email` | query | `string` | no | Filter contacts by email address. |
