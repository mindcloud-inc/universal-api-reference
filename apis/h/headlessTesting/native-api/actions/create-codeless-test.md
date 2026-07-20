# Create Codeless Test with Headless Testing

Creates a codeless test in Headless Testing.

## Endpoint

- **Method:** `POST`
- **Path:** `/lab`
- **Base URL:** `https://api.testingbot.com/v1`
- **Official documentation:** [Create Codeless Test](https://testingbot.com/support/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `test[name]` | body | `string` | yes | The codeless test name. |
| `test[url]` | body | `string` | yes | The URL to test. |
