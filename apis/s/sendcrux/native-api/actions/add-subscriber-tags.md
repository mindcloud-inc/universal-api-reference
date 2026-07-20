# Add Subscriber Tags with Sendcrux

Updates a subscriber in Sendcrux by adding tags.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/subscribers/:uid/add-tag`
- **Base URL:** `https://sendcrux.com`
- **Official documentation:** [Add Subscriber Tags](https://api.sendbound.com/subscribers/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tag` | body | `string` | yes | A comma-separated list of tags to add to the subscriber. |
| `uid` | path | `string` | yes | The unique identifier of the subscriber to tag. |
