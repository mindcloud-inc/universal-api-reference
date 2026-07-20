# Remove Background API with PiAPI/Toolkit

Creates a background-removal task in PiAPI/Toolkit.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Remove Background API](https://piapi.ai/docs/image-editing-api/remove-background-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.image` | body | `string` | yes | Doc-backed PiAPI field for Remove Background API. |
| `input.rmbg_model` | body | `string` | no | Doc-backed PiAPI field for Remove Background API. |
