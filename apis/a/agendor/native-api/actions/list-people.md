# List People with Agendor

Finds people in Agendor by search filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/people`
- **Base URL:** `https://api.agendor.com.br/v3`
- **Official documentation:** [List People](https://api.agendor.com.br/docs/#operation/List%20people)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Email prefix to search for. |
| `name` | query | `string` | no | Name prefix to search for. |
| `organization` | query | `number` | no | Organization ID to filter by. |
| `page` | query | `number` | no | Page of results to fetch. |
| `per_page` | query | `number` | no | Number of results to return per page (max 100). |
| `updatedAtGt` | query | `date` | no | Only include people updated after this ISO-8601 timestamp. |
| `updatedAtLt` | query | `date` | no | Only include people updated before this ISO-8601 timestamp. |
| `withCustomFields` | query | `boolean` | no | Include custom fields in the response. |
