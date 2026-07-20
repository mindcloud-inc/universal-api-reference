# Capture Screenshot with Custom User Agent with SCRNIFY.com

Captures a screenshot in SCRNIFY.com with a custom user agent.

## Endpoint

- **Method:** `GET`
- **Path:** `/capture`
- **Base URL:** `https://api.scrnify.com`
- **Official documentation:** [Capture Screenshot with Custom User Agent](https://scrnify.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | URL of the page to capture. |
| `userAgent` | query | `string` | no | Custom user agent string. |
