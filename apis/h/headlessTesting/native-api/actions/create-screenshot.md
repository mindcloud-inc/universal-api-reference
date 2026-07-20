# Create Screenshot with Headless Testing

Creates a screenshot job in Headless Testing.

## Endpoint

- **Method:** `POST`
- **Path:** `/screenshots`
- **Base URL:** `https://api.testingbot.com/v1`
- **Official documentation:** [Create Screenshot](https://testingbot.com/support/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `browsers` | body | `string` | yes | The browser list for the screenshot job. |
| `resolution` | body | `string` | yes | The screen resolution for the screenshot job. |
| `url` | body | `string` | yes | The page URL to capture. |
