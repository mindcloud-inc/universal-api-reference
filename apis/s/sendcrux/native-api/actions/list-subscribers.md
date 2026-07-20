# List Subscribers with Sendcrux

Retrieves subscribers from a Sendcrux email list.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/subscribers`
- **Base URL:** `https://sendcrux.com`
- **Official documentation:** [List Subscribers](https://api.sendbound.com/subscribers/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_uid` | query | `string` | yes | The unique identifier of the list whose subscribers should be returned. |
