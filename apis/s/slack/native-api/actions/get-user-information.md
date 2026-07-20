# Get User Information with Slack

Retrieves user details from a Slack workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `users.info`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [Get User Information](https://docs.slack.dev/reference/methods/users.info/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user` | query | `list` | yes | User to get info on |
| `include_locale` | query | `boolean` | no | Set this to true to receive the locale for this user. Defaults to false Format: `toggle`. |
