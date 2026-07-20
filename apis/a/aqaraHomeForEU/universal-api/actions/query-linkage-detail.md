# Aqara Home for EU: Get Linkage Details



```
GET https://connect.mindcloud.co/v1/universal/aqaraHomeForEU/latest/actions/query-linkage-detail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aqara Home for EU `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aqaraHomeForEU/latest/actions/query-linkage-detail?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aqaraHomeForEU/latest/actions/query-linkage-detail?${params}`, {
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
      "code": 1,
      "message": "string",
      "requestId": "string",
      "result": {
        "linkageId": "https://example.com",
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `message` | string |  |
| `requestId` | string |  |
| `result.linkageId` | string |  |
| `result.name` | string |  |

## Native endpoint

Through the native Aqara Home for EU API, this operation is `POST /v3.0/open/api` (base URL `https://open-ger.aqara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-linkage-detail.md) for the provider-specific parameters and requirements.

