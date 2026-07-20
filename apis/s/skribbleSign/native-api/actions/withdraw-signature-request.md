# Withdraw Signature Request with Skribble Sign

Withdraws a signature request in Skribble Sign.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/signature-requests/:signatureRequestId/withdraw`
- **Base URL:** `https://api.skribble.com`
- **Official documentation:** [Withdraw Signature Request](https://api-doc.skribble.com/#65b879fe-43ad-40bf-98a0-fe3323fcbe56)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `signatureRequestId` | path | `string` | yes | The signature request ID. |
