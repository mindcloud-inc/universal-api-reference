# Get Video Captions with Invidious

## Endpoint

- **Method:** `GET`
- **Path:** `/captions/:id`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [Get Video Captions](https://docs.invidious.io/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Video ID to fetch captions for. |
| `label` | query | `string` | no | Caption label to fetch a selected caption track. |
| `lang` | query | `string` | no | Caption language code. |
| `region` | query | `string` | no | ISO 3166 country code. |
| `tlang` | query | `string` | no | Target language for caption auto-translation. |
