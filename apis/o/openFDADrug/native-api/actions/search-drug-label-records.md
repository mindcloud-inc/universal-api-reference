# Search Drug Label Records with openFDA Drug

Finds drug label records in openFDA Drug.

## Endpoint

- **Method:** `GET`
- **Path:** `/drug/label.json`
- **Base URL:** `https://api.fda.gov`
- **Official documentation:** [Search Drug Label Records](https://open.fda.gov/apis/drug/label/how-to-use-the-endpoint/)

## Capabilities

This operation supports [filtering](../README.md#filtering) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | OpenFDA search expression, such as drug_interactions:caffeine. |
| `limit` | query | `number` | no | Maximum records to return. OpenFDA allows up to 1000 for this endpoint. |
| `skip` | query | `number` | no | Number of matching records to skip. OpenFDA supports skip values up to 25000. |
| `sort` | query | `string` | no | OpenFDA sort expression, such as effective_time:desc. |
