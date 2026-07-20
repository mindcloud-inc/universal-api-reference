# Deepset: Health

Checks the health of the Deepset service.

```
GET https://connect.mindcloud.co/v1/universal/deepset/latest/actions/health
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deepset `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepset/latest/actions/health?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepset/latest/actions/health?${params}`, {
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
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |

## Native endpoint

Through the native Deepset API, this operation is `GET /health` (base URL `https://api.cloud.deepset.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/health.md) for the provider-specific parameters and requirements.

