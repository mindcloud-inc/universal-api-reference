# Subscribe Subscriber to List with Sendcrux

Updates a Sendcrux subscriber by subscribing them to a list.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/lists/:list_uid/subscribers/:uid/subscribe`
- **Base URL:** `https://sendcrux.com`
- **Official documentation:** [Subscribe Subscriber to List](https://api.sendbound.com/subscribers/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_uid` | path | `string` | yes | The unique identifier of the parent list. |
| `uid` | path | `string` | yes | The unique identifier of the subscriber to subscribe. |
