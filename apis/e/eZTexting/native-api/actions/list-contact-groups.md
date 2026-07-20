# List Contact Groups with EZ Texting

Retrieves contact groups from EZ Texting.

## Endpoint

- **Method:** `GET`
- **Path:** `/contact-groups`
- **Base URL:** `https://a.eztexting.com/v1`
- **Official documentation:** [List Contact Groups](https://developers.eztexting.com/reference/list_2-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters[name][like]` | query | `string` | no | Filter contact groups by name |
| `page` | query | `number` | no | Page offset starting at 0 |
| `size` | query | `number` | no | Page size |
| `sort` | query | `string` | no | Sort field and direction |
