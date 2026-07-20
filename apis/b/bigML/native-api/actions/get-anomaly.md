# Get Anomaly with BigML

Retrieves an anomaly detector from BigML.

## Endpoint

- **Method:** `GET`
- **Path:** `/anomaly/:anomalyId`
- **Base URL:** `https://bigml.io`
- **Official documentation:** [Get Anomaly](https://bigml.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `anomalyId` | path | `string` | yes | BigML anomaly identifier suffix only (for example, 69cd1234abcd1234abcd1234). Do not include anomaly/. |
