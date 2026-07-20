# Create Multiple Invites with Discourse

Creates multiple user invites in Discourse.

## Endpoint

- **Method:** `POST`
- **Path:** `/invites/create-multiple.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Create Multiple Invites](https://docs.discourse.org/#tag/Invites/operation/createMultipleInvites)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Comma-separated invitee emails. |
