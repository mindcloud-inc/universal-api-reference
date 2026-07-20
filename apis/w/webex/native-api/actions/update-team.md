# Update Team with Webex

Updates an existing team in Webex.

## Endpoint

- **Method:** `PUT`
- **Path:** `/teams/:teamId`
- **Base URL:** `https://webexapis.com/v1`
- **Official documentation:** [Update Team](https://developer.webex.com/messaging/docs/api/v1/teams/update-a-team)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | Team identifier. |
| `name` | body | `string` | yes | Updated team name. |
