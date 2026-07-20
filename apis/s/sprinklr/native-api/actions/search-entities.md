# Search Entities with Sprinklr

Finds entities in Sprinklr by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `api/v2/search/{entityType}`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Search Entities](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fsearch%2F%7BentityType%7D/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `entityType` | path | `string` | yes |
| `requestBody` | body | `object` | yes |
