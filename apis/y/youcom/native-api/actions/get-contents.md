# Get Contents with You.com

Retrieves page contents from You.com.

## Endpoint

- **Method:** `POST`
- **Path:** `https://ydc-index.io/v1/contents`
- **Base URL:** `https://api.you.com`
- **Official documentation:** [Get Contents](https://docs.you.com/api-reference/contents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urls[]` | body | `array<string>` | yes | URLs to fetch. |
| `formats[]` | body | `array<string>` | no | Content formats to return. |
| `crawl_timeout` | body | `number` | no | Live crawl timeout in seconds. |
