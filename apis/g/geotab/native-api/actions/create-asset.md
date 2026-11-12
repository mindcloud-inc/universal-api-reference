# Create Asset with Geotab

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://{server}/apiv1`
- **Official documentation:** [Create Asset](https://developers.geotab.com/myGeotab/apiReference/methods/Add/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity` | body | `object` | yes | Complete Device entity to add. Required properties depend on the concrete Device type. |
