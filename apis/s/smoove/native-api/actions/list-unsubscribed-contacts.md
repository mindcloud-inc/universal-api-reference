# List Unsubscribed Contacts with Smoove

Retrieves unsubscribed contacts from Smoove.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/Contacts_Unsubscribers`
- **Base URL:** `https://rest.smoove.io`
- **Official documentation:** [List Unsubscribed Contacts](https://rest.smoove.io)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `fields` | query | `string` | no |
| `includeCustomFields` | query | `boolean` | no |
| `includeLinkedLists` | query | `boolean` | no |
