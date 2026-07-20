# Utilities - Extract URLs from Text with Encodian - Utilities

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Utilities/ExtractUrlsFromText`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Utilities - Extract URLs from Text](https://support.encodian.com/hc/en-gb/articles/11056297407261)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | The text from which URL's are to be extracted |
| `regex` | body | `string` | yes | The default regular expression used for extraction |
