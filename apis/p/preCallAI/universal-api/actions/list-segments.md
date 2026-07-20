# PreCallAI: List Segments

Retrieves segments from PreCallAI.

```
GET https://connect.mindcloud.co/v1/universal/preCallAI/latest/actions/list-segments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PreCallAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/preCallAI/latest/actions/list-segments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/preCallAI/latest/actions/list-segments?${params}`, {
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
      "data": {
        "description": "string",
        "id": "string",
        "name": "Ava Chen"
      },
      "message": "string",
      "status": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | List of segments returned by PreCallAI. |
| `data.description` | string | Segment description. |
| `data.id` | string | Segment ID. |
| `data.name` | string | Segment name. |
| `message` | string | Provider status message for listing segments. |
| `status` | number | HTTP-style status returned by PreCallAI. |
| `success` | boolean | Whether the segment list request succeeded. |

## Native endpoint

Through the native PreCallAI API, this operation is `GET /segment/list` (base URL `https://api.precallai.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-segments.md) for the provider-specific parameters and requirements.

