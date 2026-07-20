# Preserve Metadata with Tinify

Preserves metadata in an optimized image in Tinify.

## Endpoint

- **Method:** `POST`
- **Path:** `/output/:outputId`
- **Base URL:** `https://api.tinify.com`
- **Official documentation:** [Preserve Metadata](https://tinify.com/developers/reference/http#preserving-metadata)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outputId` | path | `string` | yes | Tinify output identifier from a prior compression URL. |
| `preserve[]` | body | `array<string>` | yes | Metadata fields to preserve when present in the source image. Accepted values: `0`, `1`, `2`. |
