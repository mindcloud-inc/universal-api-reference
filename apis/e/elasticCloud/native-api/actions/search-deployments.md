# Search Deployments with Elastic Cloud

Finds deployments in Elastic Cloud by query.

## Endpoint

- **Method:** `POST`
- **Path:** `/deployments/_search`
- **Base URL:** `https://api.elastic-cloud.com/api/v1`
- **Official documentation:** [Search Deployments](https://www.elastic.co/docs/api/doc/cloud/operation/operation-search-deployments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | no | Optional search query for deployment search. |
| `minimal_metadata` | query | `string` | no | Comma-separated deployment attributes to include in the minimal metadata response. |
