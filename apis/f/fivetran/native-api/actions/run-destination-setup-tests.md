# Run Destination Setup Tests with Fivetran

Runs setup tests for a destination in Fivetran.

## Endpoint

- **Method:** `POST`
- **Path:** `/destinations/[:destinationId]/test`
- **Base URL:** `https://api.fivetran.com/v1`
- **Official documentation:** [Run Destination Setup Tests](https://fivetran.com/docs/rest-api/api-reference/destination)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `destinationId` | path | `string` | yes | The unique identifier for the destination within Fivetran. |
| `trust_certificates` | body | `boolean` | no | Trust certificates automatically during destination setup tests. |
| `trust_fingerprints` | body | `boolean` | no | Trust SSH fingerprints automatically during destination setup tests. |
