# Pre-Authorize Tokenization with Payrexx

Pre-authorizes a tokenization in Payrexx.

## Endpoint

- **Method:** `POST`
- **Path:** `Transaction/:id/preAuthorize`
- **Base URL:** `https://api.payrexx.com/v1.14/`
- **Official documentation:** [Pre-Authorize Tokenization](https://developers.payrexx.com/reference/pre-authorize-a-tokenization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the transaction to pre-authorize. |
| `amount` | body | `number` | no | Amount for pre-authorization in cents. |
| `purpose` | body | `string` | no | The purpose of the pre-authorization. |
| `referenceId` | body | `string` | no | Reference ID for the pre-authorized transaction. |
