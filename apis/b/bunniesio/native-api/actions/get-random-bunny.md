# Get Random Bunny with Bunnies.io

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/loop/random/`
- **Base URL:** `https://api.bunnies.io`
- **Official documentation:** [Get Random Bunny](https://bunnies.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `media` | query | `list` | yes | One or more requested native media formats. Bunnies.io returns matching media URLs plus a poster. Accepted values: `0`, `1`, `2`, `3`. Send multiple values as a string separated by `,`. |
