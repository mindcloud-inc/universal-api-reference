# Capture Selector JPEG Screenshot with SCRNIFY.com

Captures a JPEG screenshot of a selected element with SCRNIFY.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/capture`
- **Base URL:** `https://api.scrnify.com`
- **Official documentation:** [Capture Selector JPEG Screenshot](https://scrnify.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | URL of the page to capture. |
| `selector` | query | `string` | yes | CSS selector of the element to capture. |
