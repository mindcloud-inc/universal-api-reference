# Bolna: List Providers

Retrieves providers configured in your Bolna account.

```
GET https://connect.mindcloud.co/v1/universal/bolna/latest/actions/list-providers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bolna `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bolna/latest/actions/list-providers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bolna/latest/actions/list-providers?${params}`, {
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
      "providers": [
        {}
      ],
      "providersData": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `providers` | array<object> |  |
| `providersData` | object |  |

## Native endpoint

Through the native Bolna API, this operation is `GET /providers` (base URL `https://api.bolna.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-providers.md) for the provider-specific parameters and requirements.

