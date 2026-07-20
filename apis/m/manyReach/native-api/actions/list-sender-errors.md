# List Sender Errors with ManyReach

Retrieves errors for a sender from ManyReach.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.manyreach.com/api/v2/senders/:id/errors`
- **Base URL:** `https://api.manyreach.com`
- **Official documentation:** [List Sender Errors](https://api.manyreach.com/api#v2/tag/sender)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the sender whose errors to retrieve. |
