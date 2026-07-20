# Presenton: List Presentations V3 Editor View



```
GET https://connect.mindcloud.co/v1/universal/presenton/latest/actions/list-presentations-v3-editor-view
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Presenton `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/presenton/latest/actions/list-presentations-v3-editor-view?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/presenton/latest/actions/list-presentations-v3-editor-view?${params}`, {
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
      "page": 1,
      "pageSize": 1,
      "results": [
        [
          {}
        ]
      ],
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `page` | number |  |
| `pageSize` | number |  |
| `results[]` | array<object> |  |
| `results[].createdAt` | string |  |
| `results[].id` | string |  |
| `results[].nSlides` | number |  |
| `results[].slides[]` | array<object> |  |
| `results[].slides[].id` | string |  |
| `results[].slides[].layout` | string |  |
| `results[].title` | string |  |
| `results[].type` | string |  |
| `results[].updatedAt` | string |  |
| `totalPages` | number |  |

## Native endpoint

Through the native Presenton API, this operation is `GET /api/v3/presentation/all/ui` (base URL `https://api.presenton.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-presentations-v3-editor-view.md) for the provider-specific parameters and requirements.

