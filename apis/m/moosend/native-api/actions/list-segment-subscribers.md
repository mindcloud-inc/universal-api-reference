# List Segment Subscribers with Moosend

Retrieves segment subscribers from Moosend.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/{{MailingListID}}/segments/{{SegmentID}}/members.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [List Segment Subscribers](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54618-Get-segment-subscribers?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `MailingListID` | path | `string` | yes | The ID of the email list that contains the segment. |
| `SegmentID` | path | `string` | yes | The ID of the segment that contains the subscribers you are requesting. |
