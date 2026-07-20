# List Team App Previews with Codemagic

Retrieves app previews for a specific Codemagic team.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/teams/:team_id/previews`
- **Base URL:** `https://codemagic.io`
- **Official documentation:** [List Team App Previews](https://codemagic.io/api/v3/schema#tag/App%20Previews/operation/ApiV3TeamsTeamIdPreviewsListTeamPreviews)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | yes | Codemagic team identifier. |
