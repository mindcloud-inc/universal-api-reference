# Create Browser Application with New Relic

Creates a new browser application in New Relic.

## Endpoint

- **Method:** `POST`
- **Path:** `/browser_applications.json`
- **Base URL:** `https://api.newrelic.com/v2`
- **Official documentation:** [Create Browser Application](https://docs.newrelic.com/docs/apis/rest-api-v2/browser-examples-v2/add-or-list-browser-apps-api-v2/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Browser application name. |
