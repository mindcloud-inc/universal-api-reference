# Get Transformation Project with Fivetran

Retrieves a transformation project from your Fivetran account.

## Endpoint

- **Method:** `GET`
- **Path:** `/transformation-projects/[:projectId]`
- **Base URL:** `https://api.fivetran.com/v1`
- **Official documentation:** [Get Transformation Project](https://fivetran.com/docs/rest-api/api-reference/transformation-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The unique identifier for the transformation project within Fivetran. |
