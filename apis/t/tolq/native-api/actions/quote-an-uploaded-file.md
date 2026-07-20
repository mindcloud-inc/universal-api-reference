# Quote an Uploaded File with Tolq

Creates a quote for an uploaded file in Tolq.

## Endpoint

- **Method:** `POST`
- **Path:** `/translations/requests/files/quote/:uid`
- **Base URL:** `https://api.tolq.com/v1`
- **Official documentation:** [Quote an Uploaded File](https://docs.tolq.com/reference/quote-an-uploaded-file)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | path | `string` | yes | Uploaded file UID returned by Initiate File Upload. |
| `target_language_code` | body | `string` | yes | Two-letter ISO 639-1 target language code. |
| `quality` | body | `string` | yes | Tolq quality level: machine, postediting, translation, localization, or expert. |
