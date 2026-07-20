# List Active Contacts with Smoove

Retrieves active contacts from Smoove.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/Contacts`
- **Base URL:** `https://rest.smoove.io`
- **Official documentation:** [List Active Contacts](https://rest.smoove.io)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | query | `string` | no | Comma-separated contact fields to include in the response. |
| `includeCustomFields` | query | `boolean` | no | Set to true to include contact custom fields. |
| `includeLinkedLists` | query | `boolean` | no | Set to true to include the contact's linked lists. |
