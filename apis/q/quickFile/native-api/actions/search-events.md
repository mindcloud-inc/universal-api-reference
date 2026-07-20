# Search Events with QuickFile

## Endpoint

- **Method:** `POST`
- **Path:** `/system/searchevents`
- **Base URL:** `https://api.quickfile.co.uk/1_2`
- **Official documentation:** [Search Events](https://api.quickfile.co.uk/d/v1_2/System_SearchEvents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ReturnCount` | body | `number` | no | Maximum number of QuickFile events to return. |
| `ContinuationToken` | body | `string` | no | Continuation token from a previous partial QuickFile event search response. |
| `FromDateTime` | body | `date` | no | Start of the event search range. |
| `ToDateTime` | body | `date` | no | End of the event search range. |
| `SearchType` | body | `string` | no | Optional QuickFile entity type to scope the event search. Accepted values: `0`, `1`, `2`, `3`. |
| `RefID` | body | `string` | no | Entity identifier used with SearchType. |
