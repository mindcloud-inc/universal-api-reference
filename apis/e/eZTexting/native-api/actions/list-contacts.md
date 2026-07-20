# List Contacts with EZ Texting

Retrieves contacts from EZ Texting.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://a.eztexting.com/v1`
- **Official documentation:** [List Contacts](https://developers.eztexting.com/reference/list-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters[email][like]` | query | `string` | no | Filter contacts by email |
| `filters[firstName][like]` | query | `string` | no | Filter contacts by first name |
| `filters[groupName][like]` | query | `string` | no | Filter contacts by group name |
| `filters[lastName][like]` | query | `string` | no | Filter contacts by last name |
| `filters[optOut][eq]` | query | `string` | no | Filter contacts by opt-out state |
| `filters[phoneNumber][like]` | query | `string` | no | Filter contacts by phone number |
| `filters[source][eq]` | query | `string` | no | Filter contacts by source |
| `page` | query | `number` | no | Page offset starting at 0 |
| `size` | query | `number` | no | Page size |
| `sort` | query | `string` | no | Sort field and direction |
