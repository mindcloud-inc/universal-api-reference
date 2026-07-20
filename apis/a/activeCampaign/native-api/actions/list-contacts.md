# List Contacts with ActiveCampaign

Retrieves contacts from ActiveCampaign.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `{apiUrl}/api/3`
- **Official documentation:** [List Contacts](https://developers.activecampaign.com/reference/list-all-contacts)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search contacts by name, organization, phone, or email. |
| `email` | query | `string` | no | Filter contacts by exact email. |
| `listid` | query | `string` | no | Filter contacts associated with a specific list. |
| `segmentid` | query | `string` | no | Return contacts that match the specified list segment. |
| `status` | query | `number` | no | Filter by contact status value. |
| `formid` | query | `number` | no | Filter contacts associated with a form. |
| `id_greater` | query | `number` | no | Only include contacts with ID greater than this value. |
| `id_less` | query | `number` | no | Only include contacts with ID less than this value. |
