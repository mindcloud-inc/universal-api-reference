# Download Send-To Document with Skribble Sign

Retrieves a Send-To document from Skribble Sign.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/sendto/:sendToId/download`
- **Base URL:** `https://api.skribble.com`
- **Official documentation:** [Download Send-To Document](https://api-doc.skribble.com/#2aded87e-41cf-4e07-ad94-e75d7eae7f42)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sendToId` | path | `string` | yes | The Send-To object ID. |
| `accessCode` | query | `string` | yes | The Send-To access code. This will be sent as the X-Accesscode header. |
