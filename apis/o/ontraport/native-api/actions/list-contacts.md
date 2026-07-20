# List Contacts with Ontraport

Retrieves a list of contacts from Ontraport.

## Endpoint

- **Method:** `GET`
- **Path:** `/Contacts`
- **Base URL:** `https://api.ontraport.com/1`
- **Official documentation:** [List Contacts](https://api.ontraport.com/doc/#retrieve-multiple-contacts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search the contact collection for a string. |
| `searchNotes` | query | `boolean` | no | Search notes for the search string. |
| `condition` | query | `string` | no | JSON-encoded filter criteria for selecting contacts. |
| `listFields` | query | `string` | no | Comma-delimited list of contact fields to return. |
| `externs` | query | `string` | no | Comma-delimited list of related external fields to return. |
