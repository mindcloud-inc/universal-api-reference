# Update Custom Entity with Sprinklr

Updates an existing custom entity in Sprinklr.

## Endpoint

- **Method:** `PUT`
- **Path:** `api/v2/custom-entity/entity/{entityType}/{entityId}`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Update Custom Entity](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fcustom-entity%2Fentity%2F%7BentityType%7D%2F%7BentityId%7D/put)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `entityId` | path | `string` | yes |
| `entityType` | path | `string` | yes |
| `requestBody` | body | `object` | yes |
