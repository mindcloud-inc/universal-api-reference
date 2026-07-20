# List Recent Results for Specific Group Exam with ClassMarker

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/groups/{group_id}/tests/{test_id}/recent_results.json`
- **Base URL:** `https://api.classmarker.com`
- **Official documentation:** [List Recent Results for Specific Group Exam](https://www.classmarker.com/online-testing/docs/api/#get-recent-results-for-specific-group-exam)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_id` | path | `number` | yes | Numeric ClassMarker group ID. |
| `test_id` | path | `number` | yes | Numeric ClassMarker test ID. |
| `finishedAfterTimestamp` | query | `date` | no | Only include results finished after this time. The wrapper converts the selected date to the UNIX timestamp format required by ClassMarker. |
