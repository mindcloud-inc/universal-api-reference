# List Contacts with Raklet

## Endpoint

- **Method:** `GET`
- **Path:** `/organisations/:organisationId/contacts`
- **Base URL:** `https://api.raklet.com`
- **Official documentation:** [List Contacts](https://api.raklet.com/swagger/ui/index#/Contact/Contact_GetContacts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Base64-encoded JSON filter payload used by Raklet contact search. |
