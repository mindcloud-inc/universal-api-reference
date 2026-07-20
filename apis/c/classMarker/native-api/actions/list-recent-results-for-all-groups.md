# List Recent Results for All Groups with ClassMarker

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/groups/recent_results.json`
- **Base URL:** `https://api.classmarker.com`
- **Official documentation:** [List Recent Results for All Groups](https://www.classmarker.com/online-testing/docs/api/#get-recent-results-for-all-groups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `finishedAfterTimestamp` | query | `date` | no | Only include results finished after this time. The wrapper converts the selected date to the UNIX timestamp format required by ClassMarker. |
