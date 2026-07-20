# List Applicable Plans For Resource with Acronis

Retrieves protection plans applicable to a resource in Acronis.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/policy_management/v4/policies`
- **Base URL:** `{dataCenterUrl}`
- **Official documentation:** [List Applicable Plans For Resource](https://developer.acronis.com/doc/outbound/apis/api-library/resource-policy/policies/fetching-applicable-plans-for-resource.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `applicable_to_context_id` | query | `string` | yes | Resource ID used to find applicable protection plans. |
| `include_applied_context` | query | `boolean` | no | When true, include applied context details in the response. |
