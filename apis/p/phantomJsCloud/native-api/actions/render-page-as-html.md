# Render Page as HTML with PhantomJsCloud

Renders a page as HTML in PhantomJsCloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/:apiKey/`
- **Base URL:** `https://phantomjscloud.com/api/browser/v2`
- **Official documentation:** [Render Page as HTML](https://phantomjscloud.com/docs/http-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The page URL to load and render. |
