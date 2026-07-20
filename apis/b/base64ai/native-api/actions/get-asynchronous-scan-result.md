# Get Asynchronous Scan Result with Base64.ai

Retrieves an asynchronous scan result from Base64.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/scan/async/:asyncFileUUID`
- **Base URL:** `https://base64.ai`
- **Official documentation:** [Get Asynchronous Scan Result](https://apidoc.base64.ai/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asyncFileUUID` | path | `string` | yes | Asynchronous scan identifier returned by Base64.ai. |
