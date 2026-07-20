# Search Advanced Information with Mifiel

Searches advanced document information in Mifiel.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/query`
- **Base URL:** `https://app.mifiel.com`
- **Official documentation:** [Search Advanced Information](https://docs.mifiel.com/en/#tag/Get-advanced-information/operation/QueryEndpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | body | `string` | yes | Fields to return when getting results. |
| `resource` | body | `string` | yes | Object on which the search will be made. |
| `page` | body | `number` | no | Page number to get results. |
| `per_page` | body | `number` | no | Number of records to get per page. |
| `q` | body | `object` | no | Search object keyed by field name with string or numeric term operators. |
| `sort` | body | `string` | no | Sorting method, for example created_at-desc. |
| `version` | body | `string` | no | Endpoint version. Latest documented value is 1.0.0. |
