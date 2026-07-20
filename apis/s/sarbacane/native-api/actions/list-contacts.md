# List Contacts with Sarbacane

Retrieves contacts from a Sarbacane list.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/{listId}/contacts`
- **Base URL:** `https://api.sarbacane.com/v1`
- **Official documentation:** [List Contacts](https://developers.sarbacane.com/contacts/#list-contacts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Filter contacts by exact email address. |
| `end` | query | `string` | no | Filter contacts modified on or before this ISO timestamp. |
| `listId` | path | `string` | no | Sarbacane list ID. |
| `phone` | query | `string` | no | Filter contacts by exact phone number. |
| `search` | query | `string` | no | Search text across contact fields. |
| `start` | query | `string` | no | Filter contacts modified on or after this ISO timestamp. |
