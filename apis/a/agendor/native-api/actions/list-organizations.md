# List Organizations with Agendor

Finds organizations in Agendor by search filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations`
- **Base URL:** `https://api.agendor.com.br/v3`
- **Official documentation:** [List Organizations](https://api.agendor.com.br/docs/#operation/List%20organizations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cnpj` | query | `string` | no | CNPJ prefix to search for. |
| `email` | query | `string` | no | Contact email prefix to search for. |
| `name` | query | `string` | no | Organization name prefix to search for. |
| `page` | query | `number` | no | Page of results to fetch. |
| `per_page` | query | `number` | no | Number of results to return per page (max 100). |
| `updatedAtGt` | query | `date` | no | Only include organizations updated after this ISO-8601 timestamp. |
| `updatedAtLt` | query | `date` | no | Only include organizations updated before this ISO-8601 timestamp. |
| `withCustomFields` | query | `boolean` | no | Include custom fields in the response. |
