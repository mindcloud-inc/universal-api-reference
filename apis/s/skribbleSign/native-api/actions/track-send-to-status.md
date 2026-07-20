# Track Send-To Status with Skribble Sign

Retrieves Send-To delivery status from Skribble Sign.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/sendto/:sendToId/track`
- **Base URL:** `https://api.skribble.com`
- **Official documentation:** [Track Send-To Status](https://api-doc.skribble.com/#9be42ece-fe87-4132-8d73-2c964044dc36)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sendToId` | path | `string` | yes | The Send-To object ID. |
| `accessCode` | query | `string` | yes | The Send-To access code. This will be sent as the X-Accesscode header. |
