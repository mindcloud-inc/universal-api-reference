# List APIs with RapidAPI

Retrieves APIs from RapidAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/apis`
- **Base URL:** `{baseUrlRest}`
- **Official documentation:** [List APIs](https://docs.rapidapi.com/docs/example-using-the-rest-platform-api-listing-all-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ownerId` | query | `string` | no | User or team ID that owns the APIs. |
| `visibility` | query | `string` | no | API visibility filter such as PUBLIC or PRIVATE. |
