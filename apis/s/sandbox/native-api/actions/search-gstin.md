# Search GSTIN with Sandbox

Retrieves GST registration details from Sandbox by GSTIN.

## Endpoint

- **Method:** `POST`
- **Path:** `/gst/compliance/public/gstin/search`
- **Base URL:** `https://api.sandbox.co.in`
- **Official documentation:** [Search GSTIN](https://developer.sandbox.co.in/api-reference/gst/compliance/endpoints/public/search_gstin)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `gstin` | body | `string` | yes | GSTIN to verify. |
