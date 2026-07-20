# Get Result File Content with Convertio

Retrieves converted file content from Convertio.

## Endpoint

- **Method:** `GET`
- **Path:** `/convert/:id/dl/:type`
- **Base URL:** `https://api.convertio.co`
- **Official documentation:** [Get Result File Content](https://developers.convertio.co/api/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Conversion ID returned by Start Conversion. |
| `type` | path | `string` | no | Response encoding type. Convertio documents `base64`. |
