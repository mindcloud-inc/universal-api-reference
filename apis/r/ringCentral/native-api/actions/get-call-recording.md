# Get Call Recording with RingCentral

Returns call recordings by ID(s).

## Endpoint

- **Method:** `GET`
- **Path:** `restapi/v1.0/account/:accountId/recording/:recordingId`
- **Base URL:** `https://platform.ringcentral.com/`
- **Official documentation:** [Get Call Recording](https://developers.ringcentral.com/api-reference/Call-Recordings/readCallRecording)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Internal identifier of the RingCentral account. Default value is "~" to indicate that the account associated with current authorization session should be used. |
| `recordingId` | path | `string` | yes | Internal identifier of a call recording (returned in Call Log) |
