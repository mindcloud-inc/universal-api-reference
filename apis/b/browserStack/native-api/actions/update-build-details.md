# Update Build Details with BrowserStack

Updates an existing build in BrowserStack Automate.

## Endpoint

- **Method:** `PUT`
- **Path:** `/automate/builds/:build_id.json`
- **Base URL:** `https://api.browserstack.com`
- **Official documentation:** [Update Build Details](https://www.browserstack.com/docs/automate/api-reference/selenium/build#update-build-details)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `build_id` | path | `string` | yes | BrowserStack build hashed ID from List Builds. |
| `name` | body | `string` | yes | Updated BrowserStack build name. |
