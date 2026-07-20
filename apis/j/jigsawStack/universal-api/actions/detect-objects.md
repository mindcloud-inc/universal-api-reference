# JigsawStack: Detect Objects



```
GET https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/detect-objects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JigsawStack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/detect-objects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/detect-objects?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "_usage": {},
      "annotated_image": "string",
      "gui_elements": [
        {}
      ],
      "log_id": "string",
      "objects": [
        {}
      ],
      "success": true,
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_usage` | object |  |
| `annotated_image` | string |  |
| `gui_elements` | array<object> |  |
| `log_id` | string |  |
| `objects` | array<object> |  |
| `success` | boolean |  |
| `tags` | array<string> |  |

## Native endpoint

Through the native JigsawStack API, this operation is `POST /v1/object_detection` (base URL `https://api.jigsawstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detect-objects.md) for the provider-specific parameters and requirements.

