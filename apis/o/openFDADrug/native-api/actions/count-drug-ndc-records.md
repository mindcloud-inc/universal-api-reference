# Count Drug NDC Records with openFDA Drug

Counts drug NDC records in openFDA Drug by field.

## Endpoint

- **Method:** `GET`
- **Path:** `/drug/ndc.json`
- **Base URL:** `https://api.fda.gov`
- **Official documentation:** [Count Drug NDC Records](https://open.fda.gov/apis/drug/ndc/how-to-use-the-endpoint/)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | query | `string` | yes | Field to count by. Use .exact for exact phrase buckets when OpenFDA requires it. |
| `search` | query | `string` | no | Optional OpenFDA search expression to filter records before counting. |
