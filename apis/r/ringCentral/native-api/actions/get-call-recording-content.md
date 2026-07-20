# Get Call Recording Content with RingCentral

Returns media content of a call recording (audio/mpeg or audio/wav)

## Endpoint

- **Method:** `GET`
- **Path:** `restapi/v1.0/account/:accountId/recording/:recordingId/content`
- **Base URL:** `https://platform.ringcentral.com/`
- **Official documentation:** [Get Call Recording Content](https://developers.ringcentral.com/api-reference/Call-Recordings/readCallRecording)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Internal identifier of the RingCentral account. Default value is "~" to indicate that the account associated with current authorization session should be used. |
| `contentDisposition` | query | `list<string>` | no | Whether the content is expected to be displayed in the browser, or downloaded and saved locally. |
| `contentDispositionFilename` | query | `string` | no | The default filename of the file to be downloaded |
| `recordingId` | path | `string` | yes | Internal identifier of a call recording (returned in Call Log) |
