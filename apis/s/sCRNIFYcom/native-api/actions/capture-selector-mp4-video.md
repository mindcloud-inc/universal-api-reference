# Capture Selector MP4 Video with SCRNIFY.com

Captures an MP4 video of a selected element with SCRNIFY.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/capture`
- **Base URL:** `https://api.scrnify.com`
- **Official documentation:** [Capture Selector MP4 Video](https://scrnify.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | URL of the page to capture. |
| `selector` | query | `string` | yes | CSS selector of the element to capture. |
