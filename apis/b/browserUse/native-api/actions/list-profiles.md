# List Profiles with Browser Use

Retrieves profiles from Browser Use.

## Endpoint

- **Method:** `GET`
- **Path:** `/profiles`
- **Base URL:** `https://api.browser-use.com/api/v3`
- **Official documentation:** [List Profiles](https://docs.browser-use.com/cloud/api-v3/profiles/list-profiles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageNumber` | query | `number` | no | Page number, 1-indexed. |
| `pageSize` | query | `number` | no | Number of profiles per page, maximum 100. |
| `query` | query | `string` | no | Search profiles by name or user ID. |
