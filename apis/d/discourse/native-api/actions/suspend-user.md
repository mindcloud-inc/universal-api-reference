# Suspend User with Discourse

Suspends an existing user in Discourse.

## Endpoint

- **Method:** `PUT`
- **Path:** `/admin/users/:id/suspend.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Suspend User](https://docs.discourse.org/#tag/Users/operation/suspendUser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | User id. |
| `post_action` | body | `string` | no | Optional moderation action to take on the user's posts. Accepted values: `0`. |
| `suspend_until` | body | `string` | yes | Date until the user is suspended. |
| `reason` | body | `string` | yes | Suspension reason. |
| `message` | body | `string` | no | Optional message sent with the suspension. |
