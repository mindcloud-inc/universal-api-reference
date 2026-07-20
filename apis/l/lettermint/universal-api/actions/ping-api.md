# Lettermint: Ping API

Retrieves Lettermint API status and authentication check results.

```
GET https://connect.mindcloud.co/v1/universal/lettermint/latest/actions/ping-api
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lettermint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lettermint/latest/actions/ping-api?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lettermint/latest/actions/ping-api?${params}`, {
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
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | Provider ping response body. |

## Native endpoint

Through the native Lettermint API, this operation is `GET /ping` (base URL `https://api.lettermint.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ping-api.md) for the provider-specific parameters and requirements.

