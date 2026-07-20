# Take Screenshot with Postmaster+

Takes a screenshot with the Postmaster+ API.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/screenshot/take`
- **Base URL:** `https://postmasterplus.app`
- **Official documentation:** [Take Screenshot](https://postmasterplus.app/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `device_scale` | body | `number` | no | Device scale factor from 1 to 3. |
| `format` | body | `string` | no | Image format: png, jpeg, or webp. Accepted values: `0`, `1`, `2`. |
| `height` | body | `number` | no | Viewport height in pixels, between 240 and 1080. |
| `html` | body | `string` | no | HTML content to screenshot. Required if url is not provided. |
| `url` | body | `string` | no | URL to screenshot. Required if html is not provided. |
| `width` | body | `number` | no | Viewport width in pixels, between 320 and 1920. |
