# Get Transcript with tl:dv

Retrieves a meeting transcript from tl:dv.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1alpha1/meetings/:meetingId/transcript`
- **Base URL:** `https://pasta.tldv.io`
- **Official documentation:** [Get Transcript](https://doc.tldv.io/index.html#tag/Transcripts/operation/GetTranscriptByMeetingId.GetTranscriptByMeetingId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `meetingId` | path | `string` | yes | The tl:dv meeting identifier. |
