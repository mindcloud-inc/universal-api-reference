# Search Contacts with Startquestion

Searches contacts in Startquestion.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/search`
- **Base URL:** `https://www.startquestion.com/api/v2`
- **Official documentation:** [Search Contacts](https://help.startquestion.com/en/articles/5810000-contacts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Contact email filter. |
| `label1` | query | `string` | no | First label filter. |
| `label2` | query | `string` | no | Second label filter. |
