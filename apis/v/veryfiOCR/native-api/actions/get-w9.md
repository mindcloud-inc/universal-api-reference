# Get W-9 with Veryfi OCR

Retrieves a W-9 from Veryfi OCR.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v8/partner/w9s/:document_id`
- **Base URL:** `https://api.veryfi.com/`
- **Official documentation:** [Get W-9](https://docs.veryfi.com/api/w9s/get-a-w-9/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | The Veryfi document identifier. |
