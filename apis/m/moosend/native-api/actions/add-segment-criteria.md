# Add Segment Criteria with Moosend

Adds criteria to a segment in Moosend.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists/{{MailingListID}}/segments/{{SegmentID}}/criteria/add.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [Add Segment Criteria](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54613-Add-criteria-to-a-segment?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `MailingListID` | path | `string` | yes | The ID of the email list that contains the segment. |
| `SegmentID` | path | `string` | yes | The ID of the segment. |
| `Field` | body | `string` | yes | The criterion used to filter the email list. See Field values . |
| `Comparer` | body | `string` | no | The operator that defines how to compare a Field with its Value . See Comparer values . |
| `Value` | body | `string` | no | The search term used to filter the specified Field . |
| `LastXMinutes` | body | `number` | no | Constrains the results by the time that has elapsed. |
| `DateFrom` | body | `date` | no | Constrains the results by a date span. |
| `DateTo` | body | `date` | no | Constrains the results by a date span. |
| `DateFunction` | body | `string` | no | The value used with custom fields of dateTime data type. See DateFunction values. |
