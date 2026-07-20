# Get webpage screenshot with Appwrite

Retrieves a webpage screenshot from Appwrite.

## Endpoint

- **Method:** `GET`
- **Path:** `/avatars/screenshots`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Get webpage screenshot](https://appwrite.io/docs/references/cloud/server-rest/avatars)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | Website URL which you want to capture. |
| `headers` | query | `object` | no | HTTP headers to send with the browser request. Defaults to empty. |
| `viewportWidth` | query | `number` | no | Browser viewport width. Pass an integer between 1 to 1920. Defaults to 1280. |
| `viewportHeight` | query | `number` | no | Browser viewport height. Pass an integer between 1 to 1080. Defaults to 720. |
| `scale` | query | `number` | no | Browser scale factor. Pass a number between 0.1 to 3. Defaults to 1. |
| `theme` | query | `string` | no | Browser theme. Pass "light" or "dark". Defaults to "light". |
| `userAgent` | query | `string` | no | Custom user agent string. Defaults to browser default. |
| `fullpage` | query | `boolean` | no | Capture full page scroll. Pass 0 for viewport only, or 1 for full page. Defaults to 0. |
| `locale` | query | `string` | no | Browser locale (e.g., "en-US", "fr-FR"). Defaults to browser default. |
| `timezone` | query | `string` | no | IANA timezone identifier (e.g., "America/New_York", "Europe/London"). Defaults to browser default. |
| `latitude` | query | `number` | no | Geolocation latitude. Pass a number between -90 to 90. Defaults to 0. |
| `longitude` | query | `number` | no | Geolocation longitude. Pass a number between -180 to 180. Defaults to 0. |
| `accuracy` | query | `number` | no | Geolocation accuracy in meters. Pass a number between 0 to 100000. Defaults to 0. |
| `touch` | query | `boolean` | no | Enable touch support. Pass 0 for no touch, or 1 for touch enabled. Defaults to 0. |
| `permissions[]` | query | `array<string>` | no | Browser permissions to grant. Pass an array of permission names like ["geolocation", "camera", "microphone"]. Defaults to empty. Send multiple values as a array. |
| `sleep` | query | `number` | no | Wait time in seconds before taking the screenshot. Pass an integer between 0 to 10. Defaults to 0. |
| `width` | query | `number` | no | Output image width. Pass 0 to use original width, or an integer between 1 to 2000. Defaults to 0 (original width). |
| `height` | query | `number` | no | Output image height. Pass 0 to use original height, or an integer between 1 to 2000. Defaults to 0 (original height). |
| `quality` | query | `number` | no | Screenshot quality. Pass an integer between 0 to 100. Defaults to keep existing image quality. |
| `output` | query | `string` | no | Output format type (jpeg, jpg, png, gif and webp). |
