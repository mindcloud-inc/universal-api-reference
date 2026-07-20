# Clipcat: Get Render

Retrieves a video render from Clipcat.

```
GET https://connect.mindcloud.co/v1/universal/clipcat/latest/actions/get-render
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clipcat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clipcat/latest/actions/get-render?connectionId=$CONNECTION_ID&uid=sample-render-uid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "sample-render-uid"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clipcat/latest/actions/get-render?${params}`, {
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
| `uid` | string | yes | The render UID to retrieve. Default: `sample-render-uid`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "credits": 1,
      "metadata": "string",
      "modifications": [
        {}
      ],
      "progress": 1,
      "self": "string",
      "status": "string",
      "template": "string",
      "uid": "string",
      "url": "https://example.com",
      "webhook_response_code": 1,
      "webhook_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `credits` | number |  |
| `metadata` | string |  |
| `modifications` | array<object> |  |
| `progress` | number |  |
| `self` | string |  |
| `status` | string |  |
| `template` | string |  |
| `uid` | string |  |
| `url` | string |  |
| `webhook_response_code` | number |  |
| `webhook_url` | string |  |

## Native endpoint

Through the native Clipcat API, this operation is `GET /v1/renders/:uid` (base URL `https://api.clipcat.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-render.md) for the provider-specific parameters and requirements.

