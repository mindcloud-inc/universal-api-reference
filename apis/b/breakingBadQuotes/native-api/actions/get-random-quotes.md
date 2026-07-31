# Get Random Quotes with Breaking Bad Quotes

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/quotes/:count`
- **Base URL:** `https://api.breakingbadquotes.xyz`
- **Official documentation:** [Get Random Quotes](https://github.com/shevabam/breaking-bad-quotes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | path | `number` | yes | Positive whole-number count of unique random quotes. The current first-party corpus caps requests at 174 quotes. Maximum length: 174. |
