# List Suppliers For Role with Rillion Prime

## Endpoint

- **Method:** `GET`
- **Path:** `/supplier/role/:role`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Suppliers For Role](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `role` | path | `string` | yes | Path value for Role. |
| `headersOnly` | query | `boolean` | no | When true, returns only header rows where supported. |
