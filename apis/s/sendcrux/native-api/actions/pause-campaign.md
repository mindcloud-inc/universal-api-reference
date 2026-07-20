# Pause Campaign with Sendcrux

Pauses an existing campaign in Sendcrux.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/campaigns/:uid/pause`
- **Base URL:** `https://sendcrux.com`
- **Official documentation:** [Pause Campaign](https://api.sendbound.com/campaign/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | path | `string` | yes | The unique identifier of the campaign to pause. |
