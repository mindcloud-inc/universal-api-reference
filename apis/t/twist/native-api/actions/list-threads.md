# List Threads with Twist

Retrieves threads from a Twist channel or workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/threads/get`
- **Base URL:** `https://api.twist.com/api/v3`
- **Official documentation:** [List Threads](https://developer.twist.com/v3/#get-all-threads)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after_id` | query | `number` | no | Limits threads to those with a higher id than the specified id. |
| `as_ids` | query | `boolean` | no | If enabled, only the ids of the threads are returned. |
| `before_id` | query | `number` | no | Limits threads to those with a lower id than the specified id. |
| `channel_id` | query | `number` | yes | The id of the channel. |
| `exclude_thread_ids` | query | `list<number>` | no | Thread ids that should be excluded from the results. |
| `filter_by` | query | `string` | no | A filter can be one of attached_to_me or everyone. |
| `is_pinned` | query | `boolean` | no | If enabled, only pinned threads are returned. |
| `is_starred` | query | `boolean` | no | If enabled, only starred threads are returned. |
| `limit` | query | `number` | no | Limits the number of threads returned. |
| `newer_than_ts` | query | `number` | no | Limits threads to those newer than the specified Unix time. |
| `older_than_ts` | query | `number` | no | Limits threads to those older than the specified Unix time. |
| `order_by` | query | `string` | no | Either desc or asc based on last_updated. |
| `workspace_id` | query | `number` | no | The id of the workspace. |
