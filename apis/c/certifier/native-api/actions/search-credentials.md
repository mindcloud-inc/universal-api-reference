# Search Credentials with Certifier

Finds credentials in Certifier by structured search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/credentials/search`
- **Base URL:** `https://api.certifier.io/v1`
- **Official documentation:** [Search Credentials](https://developers.certifier.io/docs/api-reference/credentials/search-credentials)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | body | `object` | yes | Structured filter object using AND/OR/NOT and field operators. |
| `sort` | body | `object` | no | — |
| `sort.property` | body | `string` | no | Sortable property such as createdAt. |
| `sort.order` | body | `string` | no | Use asc or desc. |
| `cursor` | body | `string` | no | — |
| `limit` | body | `number` | no | — |
