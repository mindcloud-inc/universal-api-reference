# Urlbox: Create Synchronous Render

Creates a synchronous render in Urlbox.

```
POST https://connect.mindcloud.co/v1/universal/urlbox/latest/actions/create-synchronous-render
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Urlbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/urlbox/latest/actions/create-synchronous-render" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/urlbox/latest/actions/create-synchronous-render', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | no | Example: `https://example.com`. |
| `html` | string | no | Example: `<html><body>Hello</body></html>`. |
| `format` | string | no | Example: `png`. |
| `width` | number | no | Example: `1280`. |
| `height` | number | no | Example: `720`. |
| `fullPage` | boolean | no |  |
| `selector` | string | no | Example: `#main`. |
| `hideCookieBanners` | boolean | no |  |
| `clickAccept` | boolean | no |  |
| `blockAds` | boolean | no |  |
| `redirectAfter` | string | no | Example: `95`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bandwidth": 1,
      "queueTime": 1,
      "renderTime": 1,
      "renderUrl": "https://example.com",
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bandwidth` | number | Bandwidth used for the generated render in bytes. |
| `queueTime` | number | Time spent waiting in queue in milliseconds. |
| `renderTime` | number | Render generation time in milliseconds. |
| `renderUrl` | string | Temporary URL pointing to the generated render. |
| `size` | number | Size of the generated render in bytes. |

## Native endpoint

Through the native Urlbox API, this operation is `POST /v1/render/sync` (base URL `https://api.urlbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-synchronous-render.md) for the provider-specific parameters and requirements.

