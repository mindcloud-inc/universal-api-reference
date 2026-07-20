# Generate All Formats For A Design with Abyssale

Generates multi-format assets asynchronously in Abyssale.

## Endpoint

- **Method:** `POST`
- **Path:** `/async/banner-builder/:design_id/generate`
- **Base URL:** `https://api.abyssale.com`
- **Official documentation:** [Generate All Formats For A Design](https://developers.abyssale.com/rest-api/generation/asynchronous-generation/generate-multi-format-images)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `design_id` | path | `string` | yes | Unique identifier (UUID) of the design to generate. |
| `elements` | body | `object` | yes | Dictionary of design elements to override for generation. |
| `callback_url` | body | `string` | no | Optional webhook URL that receives the completed batch payload. |
