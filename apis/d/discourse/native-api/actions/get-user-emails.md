# Get User Emails with Discourse

Retrieves a Discourse user's email addresses.

## Endpoint

- **Method:** `GET`
- **Path:** `/u/:username/emails.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Get User Emails](https://docs.discourse.org/#tag/Users/operation/getUserEmails)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Discourse username. |
