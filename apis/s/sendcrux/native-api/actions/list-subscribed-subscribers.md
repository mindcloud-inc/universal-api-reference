# List Subscribed Subscribers with Sendcrux

Retrieves subscribed subscribers from a Sendcrux email list.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/subscribers`
- **Base URL:** `https://sendcrux.com`
- **Official documentation:** [List Subscribed Subscribers](https://api.sendbound.com/subscribers/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_uid` | query | `string` | yes | The UID of the list whose subscribed subscribers you want to fetch. |
