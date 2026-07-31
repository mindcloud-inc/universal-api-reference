# Get Random Bunny Media with Bunnies.io

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/loop/random/redirect/`
- **Base URL:** `https://api.bunnies.io`
- **Official documentation:** [Get Random Bunny Media](https://bunnies.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `media` | query | `list` | yes | One requested native media format. The provider redirects to the raw media URL. Accepted values: `0`, `1`, `2`, `3`. |
