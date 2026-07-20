# Run Connection Setup Tests with Fivetran

Runs setup tests for a connection in Fivetran.

## Endpoint

- **Method:** `POST`
- **Path:** `/connections/[:connectionId]/test`
- **Base URL:** `https://api.fivetran.com/v1`
- **Official documentation:** [Run Connection Setup Tests](https://fivetran.com/docs/rest-api/api-reference/connection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `connectionId` | path | `string` | yes | The unique identifier for the connection within Fivetran. |
| `trust_certificates` | body | `boolean` | no | Trust certificates automatically during setup tests. |
| `trust_fingerprints` | body | `boolean` | no | Trust SSH fingerprints automatically during setup tests. |
