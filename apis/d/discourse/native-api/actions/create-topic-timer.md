# Create Topic Timer with Discourse

Creates a topic timer in Discourse.

## Endpoint

- **Method:** `POST`
- **Path:** `/t/:id/timer.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Create Topic Timer](https://docs.discourse.org/#tag/Topics/operation/createTopicTimer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `based_on_last_post` | body | `boolean` | no | Whether the timer should be based on the last post. |
| `category_id` | body | `number` | no | Optional category id used by the timer action. |
| `id` | path | `number` | yes | Topic id. |
| `time` | body | `string` | yes | Execution time for the topic timer. |
| `status_type` | body | `string` | yes | Topic timer status type. |
