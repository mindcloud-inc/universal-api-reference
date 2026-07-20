# List Read Stories with NewsBlur

Retrieves read stories from NewsBlur.

## Endpoint

- **Method:** `GET`
- **Path:** `/reader/read_stories`
- **Base URL:** `https://www.newsblur.com`
- **Official documentation:** [List Read Stories](https://newsblur.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order` | query | `string` | no | Story order: newest or oldest. Accepted values: `0`, `1`. |
