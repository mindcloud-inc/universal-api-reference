# List Occurrence Scanner Output with Intruder

## Endpoint

- **Method:** `GET`
- **Path:** `/issues/:issue_id/occurrences/:occurrence_id/scanner_output/`
- **Base URL:** `https://api.intruder.io/v1`
- **Official documentation:** [List Occurrence Scanner Output](https://developers.intruder.io/reference/issues_occurrences_scanner_output_list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `issue_id` | path | `string` | yes | The Intruder issue identifier. |
| `occurrence_id` | path | `string` | yes | The Intruder issue occurrence identifier. |
