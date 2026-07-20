# Delete Send-To with Skribble Sign

Deletes an existing Send-To request from Skribble Sign.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v2/sendto/:sendToId`
- **Base URL:** `https://api.skribble.com`
- **Official documentation:** [Delete Send-To](https://api-doc.skribble.com/#59ff33dd-6661-49eb-b4c6-b98918efeb70)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sendToId` | path | `string` | yes | The Send-To object ID. |
| `accessCode` | query | `string` | yes | The Send-To access code. This will be sent as the X-Accesscode header. |
