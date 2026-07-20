# Invite Member with WebWork Time Tracker

Invites a new member to WebWork Time Tracker.

## Endpoint

- **Method:** `POST`
- **Path:** `/members`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [Invite Member](https://api-docs.webwork-tracker.com/api/members/invitemember)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | query | `number` | yes |
| `email` | body | `string` | yes |
| `firstname` | body | `string` | yes |
| `lastname` | body | `string` | yes |
| `role` | body | `string` | yes |
