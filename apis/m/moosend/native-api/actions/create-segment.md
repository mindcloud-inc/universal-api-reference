# Create Segment with Moosend

Creates a new empty segment in Moosend.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists/{{MailingListID}}/segments/create.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [Create Segment](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54612-Create-an-empty-segment?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `MailingListID` | path | `string` | yes | The ID of the email list where the segment is created. |
| `Name` | body | `string` | yes | The name of the segment. |
| `MatchType` | body | `string` | no | Specifies how subscribers are returned by your segment based on matching criteria: All (Default) - returns subscribers that match all the given criteria. Any - returns subscribers that match any of the given criteria. |
| `FetchType` | body | `string` | no | Specifies how many criteria-matching subscribers are contained in your segment: All - returns all criteria matching subscribers. Top - returns only a maximum number of subscribers defined in  FetchValue . TopPercent - returns only a percentage of subscribers defined in  FetchValue . |
| `FetchValue` | body | `number` | no | Specifies the maximum number for FetchType:Top or percentage for FetchType:TopPercent of members to be contained in the created segment. If not specified, 0 is assumed. |
