# Count Drug Label Records with openFDA Drug

Counts drug label records in openFDA Drug by field.

## Endpoint

- **Method:** `GET`
- **Path:** `/drug/label.json`
- **Base URL:** `https://api.fda.gov`
- **Official documentation:** [Count Drug Label Records](https://open.fda.gov/apis/drug/label/how-to-use-the-endpoint/)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | query | `string` | yes | Field to count by. Use .exact for exact phrase buckets when OpenFDA requires it. |
| `search` | query | `string` | no | Optional OpenFDA search expression to filter records before counting. |
