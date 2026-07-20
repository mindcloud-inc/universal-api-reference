# Download a Meeting Transcript with Cisco Webex Meetings

Retrieves a downloadable meeting transcript from Cisco Webex Meetings.

## Endpoint

- **Method:** `GET`
- **Path:** `/meetingTranscripts/:transcriptId/download`
- **Base URL:** `https://webexapis.com/v1`
- **Official documentation:** [Download a Meeting Transcript](https://developer.webex.com/docs/api/v1/meeting-transcripts/download-a-meeting-transcript)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transcriptId` | path | `string` | yes | Unique identifier for the meeting transcript to download. |
