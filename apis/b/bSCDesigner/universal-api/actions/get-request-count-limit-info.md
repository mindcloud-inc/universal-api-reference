# BSC Designer: Get Request Count Limit Info



```
GET https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/get-request-count-limit-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BSC Designer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/get-request-count-limit-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/get-request-count-limit-info?${params}`, {
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
      "allowedCount": 1,
      "email": "ava@example.com",
      "error": {},
      "usedCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowedCount` | number |  |
| `email` | string |  |
| `error` | object |  |
| `usedCount` | number |  |

## Native endpoint

Through the native BSC Designer API, this operation is `GET /rest/api/access/info` (base URL `https://www.webbsc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-request-count-limit-info.md) for the provider-specific parameters and requirements.

