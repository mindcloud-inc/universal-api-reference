# List Recent Results for Specific Link Exam with ClassMarker

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/links/{link_id}/tests/{test_id}/recent_results.json`
- **Base URL:** `https://api.classmarker.com`
- **Official documentation:** [List Recent Results for Specific Link Exam](https://www.classmarker.com/online-testing/docs/api/#get-recent-results-for-specific-link-exam)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `link_id` | path | `number` | yes | Numeric ClassMarker link ID. |
| `test_id` | path | `number` | yes | Numeric ClassMarker test ID. |
| `finishedAfterTimestamp` | query | `date` | no | Only include results finished after this time. The wrapper converts the selected date to the UNIX timestamp format required by ClassMarker. |
