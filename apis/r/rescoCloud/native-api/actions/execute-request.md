# Execute Request with Resco Cloud

Executes a data operation in Resco Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/Execute`
- **Base URL:** `https://{organization}.app.resco.net/rest/v1/data`
- **API:** rest
- **Official documentation:** [Execute Request](https://docs.resco.net/wiki/Resco_CRM_Connector)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rawBody` | body | `string` | yes | XML request body for the Resco Execute request. |
