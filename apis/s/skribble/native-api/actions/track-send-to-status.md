# Track Send-To Status with Skribble

Retrieves the status of a Send-To request in Skribble.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/sendto/:sendToId/track`
- **Base URL:** `https://api.skribble.com`
- **Official documentation:** [Track Send-To Status](https://api-doc.skribble.com/#9be42ece-fe87-4132-8d73-2c964044dc36)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accessCode` | query | `string` | yes | The Send-To access code. This will be sent as the X-Accesscode header. |
| `sendToId` | path | `string` | yes | The Send-To object ID. |
