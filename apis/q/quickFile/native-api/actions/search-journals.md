# Search Journals with QuickFile

## Endpoint

- **Method:** `POST`
- **Path:** `/journal/search`
- **Base URL:** `https://api.quickfile.co.uk/1_2`
- **Official documentation:** [Search Journals](https://api.quickfile.co.uk/d/v1_2/Journal_Search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ReturnCount` | body | `number` | yes | Maximum number of journals to return (up to 50). |
| `Offset` | body | `number` | yes | Page offset for journal results. |
| `DateFrom` | body | `date` | no | Lower bound for the journal date range. |
| `DateTo` | body | `date` | no | Upper bound for the journal date range. |
