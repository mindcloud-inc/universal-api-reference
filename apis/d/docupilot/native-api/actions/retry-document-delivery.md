# Retry Document Delivery with Docupilot

Retries failed document delivery in Docupilot.

## Endpoint

- **Method:** `POST`
- **Path:** `/dashboard/api/v2/history/{id}/retry_delivery/`
- **Base URL:** `https://api.docupilot.app`
- **Official documentation:** [Retry Document Delivery](https://help.docupilot.app/developers/templates-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `payload` | body | `object` | yes | Provide a JSON object that matches the documented Docupilot request body. |
