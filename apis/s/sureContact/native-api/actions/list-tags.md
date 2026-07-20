# List Tags with SureContact

Retrieves available contact tags from SureContact.

## Endpoint

- **Method:** `GET`
- **Path:** `api/v1/public/tags`
- **Base URL:** `https://api.surecontact.com`
- **Official documentation:** [List Tags](https://api.surecontact.com/docs#tag-management-GETapi-v1-public-tags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `archived` | query | `string` | no | Filter tags by archive status. |
| `direction` | query | `string` | no | Sort direction: asc or desc. |
| `per_page` | query | `number` | no | Number of items per page. |
| `search` | query | `string` | no | Search tags by name or slug. |
| `sort` | query | `string` | no | Sort field. |
