# Get Bank Statement with Veryfi OCR

Retrieves a bank statement from Veryfi OCR.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v8/partner/bank-statements/:document_id`
- **Base URL:** `https://api.veryfi.com/`
- **Official documentation:** [Get Bank Statement](https://docs.veryfi.com/api/bank-statements/get-a-bank-statement/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | The Veryfi document identifier. |
