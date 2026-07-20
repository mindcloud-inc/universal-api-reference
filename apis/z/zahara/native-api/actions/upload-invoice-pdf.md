# Upload Invoice PDF with Zahara

Updates an invoice in Zahara by uploading its PDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/{businessUnitApiKey}/Invoice/Upload/{{documentId}}`
- **Base URL:** `https://api.myzahara.net`
- **Official documentation:** [Upload Invoice PDF](https://ask.zaharasoftware.com/api-docs/upload-invoice-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `number` | yes | Invoice document ID to upload into. |
