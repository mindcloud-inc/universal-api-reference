# Get Transformation with Fivetran

Retrieves a transformation from your Fivetran account.

## Endpoint

- **Method:** `GET`
- **Path:** `/transformations/[:transformationId]`
- **Base URL:** `https://api.fivetran.com/v1`
- **Official documentation:** [Get Transformation](https://fivetran.com/docs/rest-api/api-reference/transformation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transformationId` | path | `string` | yes | The unique identifier for the transformation within Fivetran. |
