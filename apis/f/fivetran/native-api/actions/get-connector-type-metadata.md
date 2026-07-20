# Get Connector Type Metadata with Fivetran

Retrieves metadata for a connector type in Fivetran.

## Endpoint

- **Method:** `GET`
- **Path:** `/metadata/connector-types/[:service]`
- **Base URL:** `https://api.fivetran.com/v1`
- **Official documentation:** [Get Connector Type Metadata](https://fivetran.com/docs/rest-api/api-reference/connector-metadata)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `service` | path | `string` | yes | The Fivetran connector type identifier. |
