# Update Topic Status with Discourse

Updates a topic's status in Discourse.

## Endpoint

- **Method:** `PUT`
- **Path:** `/t/:id/status.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Update Topic Status](https://docs.discourse.org/#tag/Topics/operation/updateTopicStatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Topic id. |
| `status` | body | `string` | yes | Topic status to change. Accepted values: `0`, `1`, `2`, `3`, `4`. |
| `enabled` | body | `string` | yes | Set true to enable the status or false to disable it. Accepted values: `0`, `1`. |
