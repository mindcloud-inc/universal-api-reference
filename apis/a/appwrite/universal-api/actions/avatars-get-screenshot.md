# Appwrite: Get webpage screenshot

Retrieves a webpage screenshot from Appwrite.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/avatars-get-screenshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/avatars-get-screenshot?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/avatars-get-screenshot?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Website URL which you want to capture. |
| `headers` | object | no | HTTP headers to send with the browser request. Defaults to empty. |
| `viewportWidth` | number | no | Browser viewport width. Pass an integer between 1 to 1920. Defaults to 1280. |
| `viewportHeight` | number | no | Browser viewport height. Pass an integer between 1 to 1080. Defaults to 720. |
| `scale` | number | no | Browser scale factor. Pass a number between 0.1 to 3. Defaults to 1. |
| `theme` | string | no | Browser theme. Pass "light" or "dark". Defaults to "light". |
| `userAgent` | string | no | Custom user agent string. Defaults to browser default. |
| `fullpage` | boolean | no | Capture full page scroll. Pass 0 for viewport only, or 1 for full page. Defaults to 0. |
| `locale` | string | no | Browser locale (e.g., "en-US", "fr-FR"). Defaults to browser default. |
| `timezone` | string | no | IANA timezone identifier (e.g., "America/New_York", "Europe/London"). Defaults to browser default. |
| `latitude` | number | no | Geolocation latitude. Pass a number between -90 to 90. Defaults to 0. |
| `longitude` | number | no | Geolocation longitude. Pass a number between -180 to 180. Defaults to 0. |
| `accuracy` | number | no | Geolocation accuracy in meters. Pass a number between 0 to 100000. Defaults to 0. |
| `touch` | boolean | no | Enable touch support. Pass 0 for no touch, or 1 for touch enabled. Defaults to 0. |
| `permissions[]` | array<string> | no | Browser permissions to grant. Pass an array of permission names like ["geolocation", "camera", "microphone"]. Defaults to empty. Accepts multiple values as an array. |
| `sleep` | number | no | Wait time in seconds before taking the screenshot. Pass an integer between 0 to 10. Defaults to 0. |
| `width` | number | no | Output image width. Pass 0 to use original width, or an integer between 1 to 2000. Defaults to 0 (original width). |
| `height` | number | no | Output image height. Pass 0 to use original height, or an integer between 1 to 2000. Defaults to 0 (original height). |
| `quality` | number | no | Screenshot quality. Pass an integer between 0 to 100. Defaults to keep existing image quality. |
| `output` | string | no | Output format type (jpeg, jpg, png, gif and webp). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object | Provider response payload. |

## Native endpoint

Through the native Appwrite API, this operation is `GET /avatars/screenshots` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/avatars-get-screenshot.md) for the provider-specific parameters and requirements.

