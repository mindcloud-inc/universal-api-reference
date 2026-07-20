# Download Quote PDF with Invoice Ninja

## Endpoint

- **Method:** `GET`
- **Path:** `/quote/:invitation_key/download`
- **Base URL:** `https://invoicing.co/api/v1`
- **Official documentation:** [Download Quote PDF](https://api-docs.invoicing.co/#tag/quotes/operation/downloadQuote)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invitation_key` | path | `string` | yes | Quote invitation key used for PDF download. |
