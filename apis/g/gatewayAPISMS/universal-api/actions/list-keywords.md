# GatewayAPI SMS: List Keywords

Retrieves configured keywords from GatewayAPI SMS.

```
GET https://connect.mindcloud.co/v1/universal/gatewayAPISMS/latest/actions/list-keywords
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatewayAPI SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gatewayAPISMS/latest/actions/list-keywords?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gatewayAPISMS/latest/actions/list-keywords?${params}`, {
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
      "keyword": "string",
      "shortcode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `keyword` | string |  |
| `shortcode` | number |  |

## Native endpoint

Through the native GatewayAPI SMS API, this operation is `GET /api/vas` (base URL `https://gatewayapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-keywords.md) for the provider-specific parameters and requirements.

