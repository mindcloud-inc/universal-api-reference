# Clipcat: List Templates

Retrieves available video templates from Clipcat.

```
GET https://connect.mindcloud.co/v1/universal/clipcat/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clipcat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clipcat/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clipcat/latest/actions/list-templates?${params}`, {
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
| `page` | number | no | The page number of template results to retrieve. |

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

Through the native Clipcat API, this operation is `GET /v1/templates` (base URL `https://api.clipcat.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

