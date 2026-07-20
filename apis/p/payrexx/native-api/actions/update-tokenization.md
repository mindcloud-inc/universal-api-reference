# Update Tokenization with Payrexx

Updates a tokenization in Payrexx.

## Endpoint

- **Method:** `PATCH`
- **Path:** `Transaction/:id/updateTokenization`
- **Base URL:** `https://api.payrexx.com/v1.14/`
- **Official documentation:** [Update Tokenization](https://developers.payrexx.com/reference/update-a-tokenization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of origin Tokenization. |
| `vatRate` | body | `number` | yes | Percentage value for new vatRate. |
