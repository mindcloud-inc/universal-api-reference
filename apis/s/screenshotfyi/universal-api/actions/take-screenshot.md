# screenshot.fyi: Take Screenshot



```
GET https://connect.mindcloud.co/v1/universal/screenshotfyi/latest/actions/take-screenshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a screenshot.fyi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/screenshotfyi/latest/actions/take-screenshot?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/screenshotfyi/latest/actions/take-screenshot?${params}`, {
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
| `url` | string | yes | The public webpage URL to capture. Example: `https://example.com`. |
| `width` | number | no | Optional viewport width in pixels. Example: `1440`. |
| `height` | number | no | Optional viewport height in pixels. Example: `900`. |
| `format` | string | no | Optional image format override. Example: `jpg`. |
| `fullPage` | boolean | no | Capture the full page instead of the default viewport. Example: `true`. |
| `darkMode` | boolean | no | Render the screenshot in dark mode when supported. Example: `false`. |
| `disableCookieBanners` | boolean | no | Remove cookie banners and similar overlays when possible. Example: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `url` | string | URL of the generated screenshot asset returned by screenshot.fyi. |

## Native endpoint

Through the native screenshot.fyi API, this operation is `GET /take` (base URL `https://screenshot.fyi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/take-screenshot.md) for the provider-specific parameters and requirements.

