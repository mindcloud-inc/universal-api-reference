# Utilities - Extract Email Addresses from Text with Encodian - Utilities

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Utilities/ExtractEmailAddressesFromText`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Utilities - Extract Email Addresses from Text](https://support.encodian.com/hc/en-gb/articles/10068475924253)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | The text from which email addresses are to be extracted |
| `regex` | body | `string` | yes | The default regular expression used for extraction |
