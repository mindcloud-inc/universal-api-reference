# DataBridge: Ping Health

Checks the DataBridge ping endpoint.

```
GET https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/ping-health
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataBridge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/ping-health?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/ping-health?${params}`, {
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
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native DataBridge API, this operation is `GET /ping` (base URL `https://api.morphik.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ping-health.md) for the provider-specific parameters and requirements.

