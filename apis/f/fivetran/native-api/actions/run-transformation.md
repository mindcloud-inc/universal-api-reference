# Run Transformation with Fivetran

Runs a transformation in your Fivetran account.

## Endpoint

- **Method:** `POST`
- **Path:** `/transformations/[:transformationId]/run`
- **Base URL:** `https://api.fivetran.com/v1`
- **Official documentation:** [Run Transformation](https://fivetran.com/docs/rest-api/api-reference/transformation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `full_refresh` | body | `boolean` | no | Run the transformation with a full refresh. |
| `transformationId` | path | `string` | yes | The unique identifier for the transformation within Fivetran. |
