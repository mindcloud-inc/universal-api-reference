# Shotstack: Get Render Status



```
GET https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/get-render-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shotstack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/get-render-status?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/get-render-status?${params}`, {
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
| `id` | string | yes | The Shotstack render ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "response": {
        "created": "string",
        "data": {},
        "duration": 1,
        "id": "string",
        "renderTime": 1,
        "status": "string",
        "updated": "string",
        "url": "https://example.com"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Status message returned by Shotstack. |
| `response.created` | string | Creation timestamp. |
| `response.data` | object | Rendered edit payload returned by Shotstack. |
| `response.duration` | number | Duration of the rendered asset in seconds. |
| `response.id` | string | Render identifier. |
| `response.renderTime` | number | Render execution time in milliseconds. |
| `response.status` | string | Current render status. |
| `response.updated` | string | Last update timestamp. |
| `response.url` | string | Temporary render output URL. |
| `success` | boolean | Whether the render status request succeeded. |

## Native endpoint

Through the native Shotstack API, this operation is `GET /edit/v1/render/:id` (base URL `https://api.shotstack.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-render-status.md) for the provider-specific parameters and requirements.

