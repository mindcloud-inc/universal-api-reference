# Delete Segment with Moosend

Deletes an existing segment from Moosend.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/lists/{{MailingListID}}/segments/{{SegmentID}}/delete.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [Delete Segment](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54616-Delete-a-segment?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `MailingListID` | path | `string` | yes | The ID of the email list that contains the segment. |
| `SegmentID` | path | `string` | yes | The ID of the segment to be deleted. |
