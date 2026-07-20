# Search Drugs@FDA Records with openFDA Drug

Finds Drugs@FDA records in openFDA Drug.

## Endpoint

- **Method:** `GET`
- **Path:** `/drug/drugsfda.json`
- **Base URL:** `https://api.fda.gov`
- **Official documentation:** [Search Drugs@FDA Records](https://open.fda.gov/apis/drug/drugsfda/how-to-use-the-endpoint/)

## Capabilities

This operation supports [filtering](../README.md#filtering) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | OpenFDA search expression. |
| `limit` | query | `number` | no | Maximum records to return. |
| `skip` | query | `number` | no | Number of matching records to skip. |
| `sort` | query | `string` | no | OpenFDA sort expression. |
