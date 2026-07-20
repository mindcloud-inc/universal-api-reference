# Create Extract Security Rules In Bulk with Sisense

Creates extract security rules in Sisense.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/elasticubes/datasecurity`
- **Base URL:** `https://signup-126940n0.sisense.com`
- **Official documentation:** [Create Extract Security Rules In Bulk](https://developer.sisense.com/guides/restApi/data-security.html#endpoints)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `[0].server` | body | `string` | yes |
| `[0].elasticube` | body | `string` | yes |
| `[0].table` | body | `string` | yes |
| `[0].column` | body | `string` | yes |
| `[0].datatype` | body | `string` | yes |
| `[0].allMembers` | body | `boolean` | yes |
| `[0].shares[0].party` | body | `string` | yes |
| `[0].shares[0].type` | body | `string` | yes |
