# Get Signature Request Report with Skribble

Retrieves a signature report for a Skribble signature request.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/signature-requests/:signatureRequestId/report`
- **Base URL:** `https://api.skribble.com`
- **Official documentation:** [Get Signature Request Report](https://api-doc.skribble.com/#cd6deb59-5d9f-47e7-9bf7-99b3bdfed8ed)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `signatureRequestId` | path | `string` | yes | The signature request ID. |
| `type` | query | `string` | no | Optional report format such as json or html. |
