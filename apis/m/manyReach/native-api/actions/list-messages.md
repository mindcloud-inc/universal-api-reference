# List Messages with ManyReach

Retrieves messages from ManyReach.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.manyreach.com/api/v2/messages`
- **Base URL:** `https://api.manyreach.com`
- **Official documentation:** [List Messages](https://api.manyreach.com/api#v2/tag/message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `string` | yes | Message type filter. Valid values: Sent, Reply, SentManual. |
