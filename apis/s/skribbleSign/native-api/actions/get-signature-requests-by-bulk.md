# Get Signature Requests By Bulk with Skribble Sign

Retrieves signature requests by bulk ID in Skribble Sign.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/signature-requests/bulk`
- **Base URL:** `https://api.skribble.com`
- **Official documentation:** [Get Signature Requests By Bulk](https://api-doc.skribble.com/#68a481be-fdb1-4474-8bd5-29df60302b76)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `signatureRequestIds[]` | body | `array<string>` | yes | The signature request IDs to fetch in bulk. |
