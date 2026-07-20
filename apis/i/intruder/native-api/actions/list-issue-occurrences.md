# List Issue Occurrences with Intruder

## Endpoint

- **Method:** `GET`
- **Path:** `/issues/:issueId/occurrences/`
- **Base URL:** `https://api.intruder.io/v1`
- **Official documentation:** [List Issue Occurrences](https://developers.intruder.io/reference/issues_occurrences_list-1)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `issue_id` | path | `string` | yes | The Intruder issue identifier. |
| `since` | query | `string` | no | Filter occurrences first detected on or after this timestamp. |
