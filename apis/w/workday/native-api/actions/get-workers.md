# Get Workers with Workday

List workers from Workday Time Tracking with optional name or worker ID search, visibility filtering, and pagination.

## Endpoint

- **Method:** `GET`
- **Path:** `workers`
- **Base URL:** `{restAPIBaseURL}/`
- **Official documentation:** [Get Workers](https://community.workday.com/sites/default/files/file-hosting/restapi/index.html#timeTracking/v5/get-/workers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search workers by name or worker ID. The search is case-insensitive. |
| `filterByOrgVisibility` | query | `boolean` | no | Only return workers whose supervisory organizations are visible to the processing user. |
| `includeTerminatedWorkers` | query | `boolean` | no | Include terminated workers in the output. |
