# WebChange Detector: Get URL

Retrieves a URL from WebChange Detector.

```
GET https://connect.mindcloud.co/v1/universal/webChangeDetector/latest/actions/get-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebChange Detector `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webChangeDetector/latest/actions/get-url?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webChangeDetector/latest/actions/get-url?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native WebChange Detector API, this operation is `GET /api/v2/urls/:id` (base URL `https://api.webchangedetector.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-url.md) for the provider-specific parameters and requirements.

