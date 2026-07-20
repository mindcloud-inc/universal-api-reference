# List Messages with EZ Texting

Retrieves messages from EZ Texting.

## Endpoint

- **Method:** `GET`
- **Path:** `/messages`
- **Base URL:** `https://a.eztexting.com/v1`
- **Official documentation:** [List Messages](https://developers.eztexting.com/reference/list_6-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters[contactNumber][eq]` | query | `string` | no | Filter messages by contact number |
| `filters[deleted][eq]` | query | `string` | no | Filter messages by deleted state |
| `filters[group][eq]` | query | `string` | no | Filter messages by group |
| `filters[incoming][eq]` | query | `string` | no | Filter messages by incoming state |
| `filters[messageId][eq]` | query | `string` | no | Filter messages by message ID |
| `filters[optType][eq]` | query | `string` | no | Filter messages by opt type |
| `filters[pending][eq]` | query | `string` | no | Filter messages by pending state |
| `filters[sentAt][gte]` | query | `string` | no | Filter messages sent at or after this time |
| `filters[sentAt][lte]` | query | `string` | no | Filter messages sent at or before this time |
| `filters[textQuery][eq]` | query | `string` | no | Filter messages by text query |
| `filters[type][eq]` | query | `string` | no | Filter messages by type |
| `filters[unread][eq]` | query | `string` | no | Filter messages by unread state |
| `filters[userNumber][eq]` | query | `string` | no | Filter messages by user number |
| `page` | query | `number` | no | Page offset starting at 0 |
| `size` | query | `number` | no | Page size |
| `sort` | query | `string` | no | Sort field and direction |
