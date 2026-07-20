# Get Custom Entity with Sprinklr

Retrieves a custom entity from Sprinklr.

## Endpoint

- **Method:** `GET`
- **Path:** `api/v2/custom-entity/entity/{entityType}/{entityId}`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Get Custom Entity](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fcustom-entity%2Fentity%2F%7BentityType%7D%2F%7BentityId%7D/get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `entityId` | path | `string` | yes |
| `entityType` | path | `string` | yes |
| `fields` | query | `string` | no |
