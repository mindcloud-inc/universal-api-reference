# Get Asset with Geotab

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://{server}/apiv1`
- **Official documentation:** [Get Asset](https://developers.geotab.com/myGeotab/apiReference/methods/Get/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `typeName` | body | `string` | yes | — |
| `search` | body | `object` | no | — |
| `search.id` | body | `string` | yes | The opaque MyGeotab Device ID. |
| `propertySelector` | body | `object` | no | — |
