# Update Segment with Moosend

Updates an existing segment in Moosend.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists/{{MailingListID}}/segments/{{SegmentID}}/update.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [Update Segment](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54617-Update-a-segment?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `MailingListID` | path | `string` | yes | The ID of the email list that contains the segment. |
| `SegmentID` | path | `string` | yes | The ID of the segment to be updated. |
| `Name` | body | `string` | no | The name of the segment. If not specified, the existing name is retained. |
| `MatchType` | body | `string` | no | Specifies how subscribers are returned by your segment based on matching criteria. If not specified, All is assumed. All (Default) - returns subscribers that match all the given criteria. Any - returns subscribers that match any of the given criteria. |
| `FetchType` | body | `string` | no | Specifies how many criteria-matching subscribers are contained in your segment. If not specified, All is assumed. All - returns all criteria matching subscribers. Top - returns only a maximum number of subscribers defined in  FetchValue . TopPercent - returns only a percentage of subscribers defined in  FetchValue . |
| `FetchValue` | body | `number` | no | Specifies the maximum number for FetchType:Top or percentage for FetchType:TopPercent of members to be contained in the created segment. If not specified, 0 is assumed. |
| `Criteria` | body | `list<object>` | no | An array containing the criteria parameters used to filter the email list. If not specified, existing criteria are retained. Field - the criterion used to filter the email list. See Field values . Comparer - the operator that defines how to compare a Field with its Value . See Comparer values . Value - the search term used to filter the specified Field . LastXMinutes - constrains the results by the time that has elapsed. DateFrom to DateTo - constrains the results by a date span. Date Function - the value used with custom fields of dateTime data type. See DateFunction values . |
