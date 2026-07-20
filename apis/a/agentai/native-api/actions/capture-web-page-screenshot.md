# Capture Web Page Screenshot with Agent.ai

Captures a web page screenshot in Agent.ai by URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/action/grab_web_screenshot`
- **Base URL:** `https://api-lr.agent.ai/v1`
- **Official documentation:** [Capture Web Page Screenshot](https://docs.agent.ai/api-reference/get-data/web-page-screenshot)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | URL of the web page to capture. |
| `ttl_for_screenshot` | body | `number` | no | Cache expiration time for the screenshot in seconds. |
