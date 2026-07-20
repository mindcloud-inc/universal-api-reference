# Update Subscriber with Sendcrux

Updates an existing subscriber in Sendcrux.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/subscribers/:uid`
- **Base URL:** `https://sendcrux.com`
- **Official documentation:** [Update Subscriber](https://api.sendbound.com/subscribers/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `EMAIL` | body | `string` | yes | The subscriber email address that Sendcrux requires on update. |
| `FIRST_NAME` | body | `string` | no | The subscriber first name. |
| `LAST_NAME` | body | `string` | no | The subscriber last name. |
| `tag` | body | `string` | no | A comma-separated list of tags to persist on the subscriber. |
| `uid` | path | `string` | yes | The unique identifier of the subscriber to update. |
