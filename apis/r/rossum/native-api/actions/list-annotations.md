# List Annotations with Rossum

Retrieves annotations from Rossum.

## Endpoint

- **Method:** `GET`
- **Path:** `/annotations`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [List Annotations](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `queue` | query | `string` | no | Queue ID filter, comma-separated for multiple values. |
| `status` | query | `string` | no | Annotation status filter; comma-separated for multiple values. |
| `page_size` | query | `number` | no | Number of results per page (max 100). |
