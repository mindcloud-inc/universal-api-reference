# Search Lines with Transport for London

Finds lines or routes in Transport for London by query.

## Endpoint

- **Method:** `GET`
- **Path:** `/Line/Search/:query`
- **Base URL:** `https://api.tfl.gov.uk`
- **Official documentation:** [Search Lines](https://api.tfl.gov.uk/swagger/ui/index.html#!/Line/Line_Search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | path | `string` | yes | Line or route search text. |
| `modes` | query | `string` | no | Optional comma-separated modes to filter line search. |
