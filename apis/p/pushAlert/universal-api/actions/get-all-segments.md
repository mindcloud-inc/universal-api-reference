# PushAlert: Get All Segments



```
GET https://connect.mindcloud.co/v1/universal/pushAlert/latest/actions/get-all-segments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PushAlert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pushAlert/latest/actions/get-all-segments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pushAlert/latest/actions/get-all-segments?${params}`, {
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
      "segments": [
        {}
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `segments` | array<object> | List of PushAlert segments returned by the API. |
| `success` | boolean | Whether the request succeeded. |

## Native endpoint

Through the native PushAlert API, this operation is `GET /rest/v2/web-push/segments` (base URL `https://api.pushalert.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-segments.md) for the provider-specific parameters and requirements.

