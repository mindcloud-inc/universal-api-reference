# Search Drug Enforcement Records with openFDA Drug

Finds drug recall enforcement records in openFDA Drug.

## Endpoint

- **Method:** `GET`
- **Path:** `/drug/enforcement.json`
- **Base URL:** `https://api.fda.gov`
- **Official documentation:** [Search Drug Enforcement Records](https://open.fda.gov/apis/drug/enforcement/how-to-use-the-endpoint/)

## Capabilities

This operation supports [filtering](../README.md#filtering) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | OpenFDA search expression. |
| `limit` | query | `number` | no | Maximum records to return. |
| `skip` | query | `number` | no | Number of matching records to skip. |
| `sort` | query | `string` | no | OpenFDA sort expression. |
