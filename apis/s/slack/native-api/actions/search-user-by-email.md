# Search User By Email with Slack

Finds a Slack user by email address.

## Endpoint

- **Method:** `GET`
- **Path:** `users.lookupByEmail`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [Search User By Email](https://docs.slack.dev/reference/methods/users.lookupByEmail/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | An email address belonging to a user in the workspace |
