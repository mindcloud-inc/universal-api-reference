# Get Asset Group with Geotab

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://{server}/apiv1`
- **Official documentation:** [Get Asset Group](https://developers.geotab.com/myGeotab/apiReference/methods/Get/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `method` | body | `string` | yes | — |
| `typeName` | body | `string` | yes | — |
| `search` | body | `object` | no | — |
| `search.id` | body | `string` | yes | The opaque MyGeotab Group ID. |
| `propertySelector` | body | `object` | no | — |
