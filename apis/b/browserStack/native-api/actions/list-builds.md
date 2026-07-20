# List Builds with BrowserStack

Retrieves build records from BrowserStack Automate.

## Endpoint

- **Method:** `GET`
- **Path:** `/automate/builds.json`
- **Base URL:** `https://api.browserstack.com`
- **Official documentation:** [List Builds](https://www.browserstack.com/docs/automate/api-reference/selenium/build#get-build-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of builds to return. |
| `offset` | query | `number` | no | Offset for build list pagination. |
| `status` | query | `string` | no | Build status filter: running, done, timeout, or failed. |
| `projectId` | query | `number` | no | Filter builds by BrowserStack project ID. |
