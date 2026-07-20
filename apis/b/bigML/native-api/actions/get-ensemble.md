# Get Ensemble with BigML

Retrieves an ensemble from BigML.

## Endpoint

- **Method:** `GET`
- **Path:** `/ensemble/:ensembleId`
- **Base URL:** `https://bigml.io`
- **Official documentation:** [Get Ensemble](https://bigml.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ensembleId` | path | `string` | yes | BigML ensemble identifier suffix only (for example, 69cd1234abcd1234abcd1234). Do not include ensemble/. |
