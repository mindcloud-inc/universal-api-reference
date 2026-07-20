# Patch Standard Entity with Sprinklr

Updates part of a standard entity in Sprinklr.

## Endpoint

- **Method:** `PATCH`
- **Path:** `api/v2/standard-entity/entity/{entityType}/{entityId}`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Patch Standard Entity](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fstandard-entity%2Fentity%2F%7BentityType%7D%2F%7BentityId%7D/patch)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `entityId` | path | `string` | yes |
| `entityType` | path | `string` | yes |
| `requestBody` | body | `object` | yes |
