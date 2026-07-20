# Update Segment Criteria with Moosend

Updates segment criteria in Moosend.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists/{{MailingListID}}/segments/{{SegmentID}}/criteria/{{CriteriaID}}/update.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [Update Segment Criteria](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54615-Update-segment-criteria?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `MailingListID` | path | `string` | yes | The ID of the email list that contains the segment. |
| `SegmentID` | path | `string` | yes | The ID of the segment. |
| `CriteriaID` | path | `string` | yes | The ID of the criteria of a segment to be updated. |
| `Field` | body | `string` | yes | The criterion used to filter the email list. See Field values . |
| `Comparer` | body | `string` | no | The operator that defines how to compare a Field with its Value . See Comparer values. |
| `Value` | body | `string` | no | The search term used to filter the specified Field . |
| `LastXMinutes` | body | `number` | no | Constrains the results by the time that has elapsed. |
| `DateFrom` | body | `date` | no | Constrains the results by a date span. |
| `DateTo` | body | `date` | no | Constrains the results by a date span. |
| `DateFunction` | body | `string` | no | The value used with custom fields of dateTime data type. See DateFunction values . |
