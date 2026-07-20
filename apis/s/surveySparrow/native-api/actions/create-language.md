# Create Language with SurveySparrow

Creates a custom language in SurveySparrow.

## Endpoint

- **Method:** `POST`
- **Path:** `/language`
- **Base URL:** `https://api.surveysparrow.com/v3`
- **Official documentation:** [Create Language](https://developers.surveysparrow.com/rest-apis/post-v-3-language/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language_name` | body | `string` | yes | Custom language name |
| `language_code` | body | `string` | yes | Three-letter custom language code |
