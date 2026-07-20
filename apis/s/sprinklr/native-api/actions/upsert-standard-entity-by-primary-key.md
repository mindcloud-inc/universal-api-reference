# Upsert Standard Entity By Primary Key with Sprinklr

Updates or creates a standard entity in Sprinklr by primary key.

## Endpoint

- **Method:** `POST`
- **Path:** `api/v2/standard-entity/entity/upsertByPrimaryKey/{entityType}`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Upsert Standard Entity By Primary Key](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fstandard-entity%2Fentity%2FupsertByPrimaryKey%2F%7BentityType%7D/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `entityType` | path | `string` | yes |
| `requestBody` | body | `object` | yes |
