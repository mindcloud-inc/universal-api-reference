# Invite User to Team with Push by Techulus

## Endpoint

- **Method:** `POST`
- **Path:** `/api/management/v1/teams/invite`
- **Base URL:** `https://push.techulus.com`
- **Official documentation:** [Invite User to Team](https://docs.push.techulus.com/management-api-beta)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team` | body | `string` | yes | Team API key supplied from the connection Team credential. |
| `email` | body | `string` | yes | Email address of the user to invite to the team. |
