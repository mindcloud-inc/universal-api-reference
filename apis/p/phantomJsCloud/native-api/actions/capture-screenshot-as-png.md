# Capture Screenshot as PNG with PhantomJsCloud

Captures a page screenshot as PNG in PhantomJsCloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/:apiKey/`
- **Base URL:** `https://phantomjscloud.com/api/browser/v2`
- **Official documentation:** [Capture Screenshot as PNG](https://phantomjscloud.com/docs/http-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The page URL to load and render. |
