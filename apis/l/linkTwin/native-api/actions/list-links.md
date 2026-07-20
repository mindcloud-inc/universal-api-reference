# List Links with LinkTwin

Retrieves your shortened links from LinkTwin.

## Endpoint

- **Method:** `GET`
- **Path:** `/urls`
- **Base URL:** `https://linktw.in/api`
- **Official documentation:** [List Links](https://linktw.in/developers#list-links)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Per page data result. |
| `page` | query | `number` | no | Current page request. |
| `order` | query | `string` | no | Sort order. |
| `search` | query | `string` | no | Search links. |
| `date_from` | query | `string` | no | Start date filter. |
| `date_to` | query | `string` | no | End date filter. |
| `collections` | query | `string` | no | JSON array string of collection IDs or names. |
| `timezone` | query | `string` | no | Timezone override for response dates. |
