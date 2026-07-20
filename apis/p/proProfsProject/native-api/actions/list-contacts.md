# List Contacts with ProProfs Project

Retrieves a list of contacts from ProProfs Project.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [List Contacts](https://help.proprofsproject.com/managing-contacts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | query | `string` | no | Show contacts for a particular client. |
| `limit` | query | `string` | no | Limit the number of returned contacts. |
| `offset` | query | `string` | no | Offset for returned contacts. |
