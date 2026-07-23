# List Companies By Role with Rillion Prime

## Endpoint

- **Method:** `GET`
- **Path:** `/company/role/:role`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Companies By Role](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html?urls.primaryName=MasterData%20-%20v1.0)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `role` | path | `string` | yes | Role name to use in the path, for example Administrator. |
| `headersOnly` | query | `boolean` | no | When true, returns only header rows where supported. |
