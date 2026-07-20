# Get Model with BigML

Retrieves a model from BigML.

## Endpoint

- **Method:** `GET`
- **Path:** `/model/:modelId`
- **Base URL:** `https://bigml.io`
- **Official documentation:** [Get Model](https://bigml.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modelId` | path | `string` | yes | BigML model identifier suffix only (for example, 69cd1234abcd1234abcd1234). Do not include model/. |
