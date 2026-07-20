# Get Resource Details with Acronis

Retrieves detailed information about a resource from Acronis.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/resource_management/v4/resources/{resource_id}/attributes`
- **Base URL:** `{dataCenterUrl}`
- **Official documentation:** [Get Resource Details](https://developer.acronis.com/doc/outbound/apis/api-library/resource-policy/resources/fetching-resource-info.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resource_id` | path | `string` | yes | Resource Id path parameter. |
