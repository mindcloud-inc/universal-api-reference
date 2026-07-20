# Get Evaluation with BigML

Retrieves an evaluation from BigML.

## Endpoint

- **Method:** `GET`
- **Path:** `/evaluation/:evaluationId`
- **Base URL:** `https://bigml.io`
- **Official documentation:** [Get Evaluation](https://bigml.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `evaluationId` | path | `string` | yes | BigML evaluation identifier suffix only (for example, 69cd1234abcd1234abcd1234). Do not include evaluation/. |
