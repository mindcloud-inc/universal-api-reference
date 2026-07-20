# Update Signature Request Signers with Skribble

Updates the signer list for a signature request in Skribble.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/signature-requests`
- **Base URL:** `https://api.skribble.com`
- **Official documentation:** [Update Signature Request Signers](https://api-doc.skribble.com/#c1a29021-bb26-40af-9bd2-c4a774e4a18d)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The signature request ID to update. |
| `signatures[]` | body | `array<object>` | yes | The complete signer list to keep on the signature request. |
| `title` | body | `string` | no | Optional replacement title. |
