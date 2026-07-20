# List Pipelines with Streak

Retrieves pipelines from Streak.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/pipelines`
- **Base URL:** `https://api.streak.com`
- **Official documentation:** [List Pipelines](https://streak.readme.io/reference/list-all-pipelines)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sortBy` | query | `list<string>` | no | What order to sort the pipelines by. Valid values are creationTimestamp and lastUpdatedTimestamp. Accepted values: `creationTimestamp`, `lastUpdatedTimestamp`. |
