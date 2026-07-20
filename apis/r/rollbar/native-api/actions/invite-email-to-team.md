# Invite Email To Team with Rollbar

Creates a team invitation in Rollbar.

## Endpoint

- **Method:** `POST`
- **Path:** `/team/:teamId/invites`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Invite Email To Team](https://docs.rollbar.com/reference/invite-an-email-address-to-a-team)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address to invite to the team |
| `teamId` | path | `number` | yes | Rollbar team identifier |
