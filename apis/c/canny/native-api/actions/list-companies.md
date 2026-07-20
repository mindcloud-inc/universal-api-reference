# List Companies with Canny

Retrieves all available companies from Canny.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/companies/list`
- **Base URL:** `https://canny.io/api`
- **Official documentation:** [List Companies](https://developers.canny.io/api-reference#list_companies)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `search` | body | `string` | no |
| `segment` | body | `string` | no |
| `limit` | body | `number` | no |
| `cursor` | body | `string` | no |
