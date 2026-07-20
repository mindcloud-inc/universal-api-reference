# Search Stop Points with Transport for London

Finds stop points in Transport for London by name or code.

## Endpoint

- **Method:** `GET`
- **Path:** `/StopPoint/Search/:query`
- **Base URL:** `https://api.tfl.gov.uk`
- **Official documentation:** [Search Stop Points](https://api.tfl.gov.uk/swagger/ui/index.html#!/StopPoint/StopPoint_Search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | path | `string` | yes | Stop point search text, common name, or 5-digit Countdown bus stop code. |
| `modes` | query | `string` | no | Optional comma-separated modes to filter stop point search. |
| `maxResults` | query | `number` | no | Optional maximum number of search results. TfL defaults to and caps this at 50. |
