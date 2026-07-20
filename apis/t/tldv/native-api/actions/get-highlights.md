# Get Highlights with tl:dv

Retrieves deprecated meeting highlights from tl:dv.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1alpha1/meetings/:meetingId/highlights`
- **Base URL:** `https://pasta.tldv.io`
- **Official documentation:** [Get Highlights](https://doc.tldv.io/index.html#tag/Highlights-(deprecated)/operation/GetHighlightsByMeetingId.getHighlightsByMeetingId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `meetingId` | path | `string` | yes | The tl:dv meeting identifier. |
