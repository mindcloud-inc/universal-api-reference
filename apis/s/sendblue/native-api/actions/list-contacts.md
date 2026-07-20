# List Contacts with Sendblue

Retrieves a list of contacts from Sendblue.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/contacts`
- **Base URL:** `https://api.sendblue.co`
- **Official documentation:** [List Contacts](https://docs.sendblue.com/api/resources/contacts/methods/list/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cid` | query | `string` | no | Filter contacts by Sendblue contact ID. |
| `phone_number` | query | `string` | no | Filter contacts by phone number. |
