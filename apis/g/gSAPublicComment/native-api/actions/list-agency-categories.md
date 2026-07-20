# List Agency Categories with GSA Public Comment

Retrieves agency categories for an acronym from GSA Public Comment.

## Endpoint

- **Method:** `GET`
- **Path:** `/agency-categories`
- **Base URL:** `https://api.regulations.gov/v4`
- **Official documentation:** [List Agency Categories](https://open.gsa.gov/api/regulationsgov/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[acronym]` | query | `string` | yes | Agency acronym, such as FAA. |
