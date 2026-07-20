# ThriveDesk: Search



```
GET https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThriveDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/search?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/search?${params}`, {
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
      "data": {},
      "items": [
        {}
      ],
      "page": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Raw response payload. |
| `items` | array<object> | Returned Search Result records. |
| `page` | number | Current result page when returned. |
| `total` | number | Total record count when returned. |

## Native endpoint

Through the native ThriveDesk API, this operation is `POST /v1/search` (base URL `https://api.thrivedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search.md) for the provider-specific parameters and requirements.

