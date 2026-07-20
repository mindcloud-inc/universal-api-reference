# List Dynamic Set Values with ServiceTitan

Retrieves dynamic set values from ServiceTitan.

## Endpoint

- **Method:** `GET`
- **Path:** `reporting/v2/tenant/{tenant}/dynamic-value-sets/:dynamicSetId`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [List Dynamic Set Values](https://developer.servicetitan.io/docs/apis/tenant-reporting-v2/endpoints/DynamicValueSets_GetDynamicSet)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dynamicSetId` | path | `string` | yes | ID of dynamic set taken from a report description. |
| `includeTotal` | query | `boolean` | no | Whether total count should be returned. |
