# Merge Renders with Templated

Merges existing renders together in Templated.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/render/merge`
- **Base URL:** `https://api.templated.io`
- **Official documentation:** [Merge Renders](https://templated.io/docs/renders/merge/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<string>` | yes | The render ids of the renders that will be merged. |
| `host` | body | `boolean` | no | When true, the merged PDF will be hosted and the response will include a URL. |
| `urls[]` | body | `array<string>` | no | Optional array of PDF URLs to merge with the renders. |
