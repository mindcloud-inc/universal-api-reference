# Count Drug Shortage Records with openFDA Drug

Counts drug shortage records in openFDA Drug by field.

## Endpoint

- **Method:** `GET`
- **Path:** `/drug/shortages.json`
- **Base URL:** `https://api.fda.gov`
- **Official documentation:** [Count Drug Shortage Records](https://open.fda.gov/apis/drug/drugshortages/how-to-use-the-endpoint/)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | query | `string` | yes | Field to count by. Use .exact for exact phrase buckets when OpenFDA requires it. |
| `search` | query | `string` | no | Optional OpenFDA search expression to filter records before counting. |
