# Count Drugs@FDA Records with openFDA Drug

Counts Drugs@FDA records in openFDA Drug by field.

## Endpoint

- **Method:** `GET`
- **Path:** `/drug/drugsfda.json`
- **Base URL:** `https://api.fda.gov`
- **Official documentation:** [Count Drugs@FDA Records](https://open.fda.gov/apis/drug/drugsfda/how-to-use-the-endpoint/)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | query | `string` | yes | Field to count. Use exact fields supported by openFDA Drugs@FDA, such as products.brand_name.exact, products.dosage_form.exact, or products.route.exact. |
| `search` | query | `string` | no | Optional OpenFDA search expression to filter records before counting. |
