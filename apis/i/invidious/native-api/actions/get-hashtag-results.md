# Get Hashtag Results with Invidious

## Endpoint

- **Method:** `GET`
- **Path:** `/hashtag/:tag`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [Get Hashtag Results](https://docs.invidious.io/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Hashtag result page number. |
| `tag` | path | `string` | yes | Hashtag without the # prefix. |
