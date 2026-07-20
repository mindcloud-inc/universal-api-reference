# DataBridge: Get Logs

Retrieves audit logs from DataBridge.

```
GET https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/get-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataBridge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/get-logs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/get-logs?${params}`, {
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
      "items": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |

## Native endpoint

Through the native DataBridge API, this operation is `GET /logs/` (base URL `https://api.morphik.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-logs.md) for the provider-specific parameters and requirements.

