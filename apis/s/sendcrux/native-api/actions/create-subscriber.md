# Create Subscriber with Sendcrux

Creates a new subscriber in a Sendcrux email list.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/subscribers`
- **Base URL:** `https://sendcrux.com`
- **Official documentation:** [Create Subscriber](https://api.sendbound.com/subscribers/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `EMAIL` | body | `string` | yes | The subscriber email address. |
| `FIRST_NAME` | body | `string` | no | The subscriber first name. |
| `LAST_NAME` | body | `string` | no | The subscriber last name. |
| `list_uid` | body | `string` | yes | The unique identifier of the list that should receive the subscriber. |
| `tag` | body | `string` | no | A comma-separated list of tags to assign to the subscriber. |
