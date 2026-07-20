# Northflank: Get API status

Retrieves the current Northflank API status.

```
GET https://connect.mindcloud.co/v1/universal/northflank/latest/actions/get-api-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Northflank `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/northflank/latest/actions/get-api-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/northflank/latest/actions/get-api-status?${params}`, {
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Northflank API, this operation is `GET /` (base URL `https://api.northflank.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-status.md) for the provider-specific parameters and requirements.

