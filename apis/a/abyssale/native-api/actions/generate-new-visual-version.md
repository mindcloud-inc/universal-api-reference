# Generate New Visual Version with Abyssale

Generates a new visual variation in Abyssale.

## Endpoint

- **Method:** `POST`
- **Path:** `/banner-builder/:designId/generate`
- **Base URL:** `https://api.abyssale.com`
- **Official documentation:** [Generate New Visual Version](https://developers.abyssale.com/rest-api/generation/visual-versioning)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `designId` | path | `string` | yes | Design ID to generate from |
| `elements` | body | `object` | yes | Customization payload for design elements |
| `original_visual_id` | body | `string` | yes | Existing visual ID to create a new version for |
