# Get Rich Snippet with ProvenExpert

Retrieves rich snippet HTML for ProvenExpert ratings.

## Endpoint

- **Method:** `POST`
- **Path:** `/rating/summary/richsnippet`
- **Base URL:** `https://www.provenexpert.com/api/v1`
- **Official documentation:** [Get Rich Snippet](https://developer.provenexpert.com/index_en.html#rating-summary-richsnippet)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.version` | body | `number` | no | Display mode for the stars. |
| `data.strokeColor` | body | `string` | no | Line color of the stars as a hex string. |
| `data.fillColor` | body | `string` | no | Fill color of the stars as a hex string. |
| `data.fontColor` | body | `string` | no | Text color as a hex string. |
