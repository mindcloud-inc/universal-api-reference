# Download Send-To Document with Skribble

Retrieves the current document for a Send-To request in Skribble.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/sendto/:sendToId/download`
- **Base URL:** `https://api.skribble.com`
- **Official documentation:** [Download Send-To Document](https://api-doc.skribble.com/#2aded87e-41cf-4e07-ad94-e75d7eae7f42)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accessCode` | query | `string` | yes | The Send-To access code. This will be sent as the X-Accesscode header. |
| `sendToId` | path | `string` | yes | The Send-To object ID. |
