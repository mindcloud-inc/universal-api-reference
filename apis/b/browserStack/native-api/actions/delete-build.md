# Delete Build with BrowserStack

Deletes an existing build from BrowserStack Automate.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/automate/builds/:build_id.json`
- **Base URL:** `https://api.browserstack.com`
- **Official documentation:** [Delete Build](https://www.browserstack.com/docs/automate/api-reference/selenium/build#delete-build)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `build_id` | path | `string` | yes | BrowserStack hashed build ID. |
