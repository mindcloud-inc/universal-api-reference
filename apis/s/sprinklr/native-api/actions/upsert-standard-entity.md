# Upsert Standard Entity with Sprinklr

Updates or creates a standard entity in Sprinklr.

## Endpoint

- **Method:** `POST`
- **Path:** `api/v2/standard-entity/entity/upsert/{entityType}/{entityId}`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Upsert Standard Entity](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fstandard-entity%2Fentity%2Fupsert%2F%7BentityType%7D%2F%7BentityId%7D/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `entityId` | path | `string` | yes |
| `entityType` | path | `string` | yes |
| `requestBody` | body | `object` | yes |
