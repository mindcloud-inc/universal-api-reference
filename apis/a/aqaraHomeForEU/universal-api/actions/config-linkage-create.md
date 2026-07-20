# Aqara Home for EU: Create Linkage



```
POST https://connect.mindcloud.co/v1/universal/aqaraHomeForEU/latest/actions/config-linkage-create
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aqara Home for EU `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aqaraHomeForEU/latest/actions/config-linkage-create" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aqaraHomeForEU/latest/actions/config-linkage-create', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
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
        "linkageId": "https://example.com"
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

## Native endpoint

Through the native Aqara Home for EU API, this operation is `POST /v3.0/open/api` (base URL `https://open-ger.aqara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/config-linkage-create.md) for the provider-specific parameters and requirements.

