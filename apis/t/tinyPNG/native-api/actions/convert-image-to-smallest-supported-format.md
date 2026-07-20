# Convert Image To Smallest Supported Format with TinyPNG

Creates the smallest supported image format in TinyPNG.

## Endpoint

- **Method:** `POST`
- **Path:** `{{outputPath}}`
- **Base URL:** `https://api.tinify.com`
- **Official documentation:** [Convert Image To Smallest Supported Format](https://tinify.com/developers/reference/http#converting-images)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outputPath` | path | `string` | yes | TinyPNG output path returned by a previous action, for example `/output/abc123`. |
