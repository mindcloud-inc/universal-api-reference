# Count Drug Adverse Event Records with openFDA Drug

Counts drug adverse event records in openFDA Drug by field.

## Endpoint

- **Method:** `GET`
- **Path:** `/drug/event.json`
- **Base URL:** `https://api.fda.gov`
- **Official documentation:** [Count Drug Adverse Event Records](https://open.fda.gov/apis/drug/event/how-to-use-the-endpoint/)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | query | `string` | yes | Field to count by. Use .exact for exact phrase buckets when OpenFDA requires it. |
| `search` | query | `string` | no | Optional OpenFDA search expression to filter records before counting. |
