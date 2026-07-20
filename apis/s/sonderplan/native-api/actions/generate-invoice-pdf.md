# Generate Invoice PDF with Sonderplan

## Endpoint

- **Method:** `GET`
- **Path:** `/invoice/pdf`
- **Base URL:** `https://api.sonderplan.com/v2`
- **Official documentation:** [Generate Invoice PDF](https://docs.sonderplan.com/api-reference/invoice/generate-invoice-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | Invoice ID to generate a PDF for. |
