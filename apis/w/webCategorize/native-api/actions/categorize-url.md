# Categorize URL with WebCategorize

## Endpoint

- **Method:** `POST`
- **Path:** `/url`
- **Base URL:** `https://app.webcategorize.com/api`
- **Official documentation:** [Categorize URL](https://webcategorize.com/webcategorize.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | URL to fetch and categorize. |
| `tags[]` | body | `array<string>` | no | Optional tags to store with the URL submission. |
| `cache` | body | `boolean` | no | Set true to look for an existing categorization of this URL. |
