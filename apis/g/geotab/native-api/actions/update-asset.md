# Update Asset with Geotab

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://{server}/apiv1`
- **Official documentation:** [Update Asset](https://developers.geotab.com/myGeotab/apiReference/methods/Set/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity` | body | `object` | yes | Complete current Device entity with the intended changes. Set is not a JSON Patch; preserve the ID and all other required properties. |
