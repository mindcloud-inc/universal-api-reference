# List Surveys with Survicate

Retrieves surveys from your Survicate workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/surveys`
- **Base URL:** `https://data-api.survicate.com/v2`
- **Official documentation:** [List Surveys](https://developers.survicate.com/data-export/survey/#list-all-surveys)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | query | `string` | no | Filter surveys created before or at this ISO 8601 timestamp with microseconds. |
| `end` | query | `string` | no | Filter surveys created on or after this ISO 8601 timestamp with microseconds. |
