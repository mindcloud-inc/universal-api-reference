# Preserve Copyright And Creation Metadata with TinyPNG

Preserves copyright and creation metadata in TinyPNG output.

## Endpoint

- **Method:** `POST`
- **Path:** `{{outputPath}}`
- **Base URL:** `https://api.tinify.com`
- **Official documentation:** [Preserve Copyright And Creation Metadata](https://tinify.com/developers/reference/http#preserving-metadata)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outputPath` | path | `string` | yes | TinyPNG output path returned by a previous action, for example `/output/abc123`. |
