# Render Page as PDF with PhantomJsCloud

Renders a page as PDF in PhantomJsCloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/:apiKey/`
- **Base URL:** `https://phantomjscloud.com/api/browser/v2`
- **Official documentation:** [Render Page as PDF](https://phantomjscloud.com/docs/http-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The page URL to load and render. |
