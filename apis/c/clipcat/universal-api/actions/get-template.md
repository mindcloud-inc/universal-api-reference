# Clipcat: Get Template

Retrieves a video template from Clipcat.

```
GET https://connect.mindcloud.co/v1/universal/clipcat/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clipcat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clipcat/latest/actions/get-template?connectionId=$CONNECTION_ID&uid=sample-template-uid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "sample-template-uid"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clipcat/latest/actions/get-template?${params}`, {
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
| `uid` | string | yes | The template UID to retrieve. Default: `sample-template-uid`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "frame_rate": 1,
      "height": 1,
      "scenes": [
        {}
      ],
      "self": "string",
      "title": "string",
      "type": "string",
      "uid": "string",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `frame_rate` | number |  |
| `height` | number |  |
| `scenes` | array<object> |  |
| `self` | string |  |
| `title` | string |  |
| `type` | string |  |
| `uid` | string |  |
| `width` | number |  |

## Native endpoint

Through the native Clipcat API, this operation is `GET /v1/templates/:uid` (base URL `https://api.clipcat.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.

