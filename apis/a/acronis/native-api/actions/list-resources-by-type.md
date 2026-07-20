# List Resources By Type with Acronis

Retrieves resources by type from Acronis.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/resource_management/v4/resources`
- **Base URL:** `{dataCenterUrl}`
- **Official documentation:** [List Resources By Type](https://developer.acronis.com/doc/outbound/apis/api-library/resource-policy/resources/fetching-resources-by-type.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `string` | yes | Resource type filter, for example resource.machine. |
