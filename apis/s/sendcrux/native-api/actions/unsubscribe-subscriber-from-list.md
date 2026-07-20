# Unsubscribe Subscriber from List with Sendcrux

Updates a Sendcrux subscriber by unsubscribing them from a list.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/lists/:list_uid/subscribers/:uid/unsubscribe`
- **Base URL:** `https://sendcrux.com`
- **Official documentation:** [Unsubscribe Subscriber from List](https://api.sendbound.com/subscribers/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_uid` | path | `string` | yes | The unique identifier of the parent list. |
| `uid` | path | `string` | yes | The unique identifier of the subscriber to unsubscribe. |
