# Run Browser Function with Browserless

Runs custom browser code in Browserless.

## Endpoint

- **Method:** `POST`
- **Path:** `/function`
- **Base URL:** `https://production-sfo.browserless.io`
- **Official documentation:** [Run Browser Function](https://docs.browserless.io/rest-apis/function)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | body | `string` | yes | JavaScript function code to execute in the browser. |
| `context` | body | `object` | no | Optional JSON object passed to the function as context. |
