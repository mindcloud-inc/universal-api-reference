# Get Segment Details with Moosend

Retrieves segment details from Moosend.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/{{MailingListID}}/segments/{{SegmentID}}/details.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [Get Segment Details](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54619-Get-segment-details?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `MailingListID` | path | `string` | yes | The ID of the email list that contains the segment. |
| `SegmentID` | path | `string` | yes | The ID of the segment that contains the details you are requesting. |
