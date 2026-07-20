# List Recent Results for All Links with ClassMarker

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/links/recent_results.json`
- **Base URL:** `https://api.classmarker.com`
- **Official documentation:** [List Recent Results for All Links](https://www.classmarker.com/online-testing/docs/api/#get-recent-results-for-all-links)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `finishedAfterTimestamp` | query | `date` | no | Only include results finished after this time. The wrapper converts the selected date to the UNIX timestamp format required by ClassMarker. |
