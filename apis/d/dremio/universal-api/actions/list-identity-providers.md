# Dremio: List Identity Providers

Retrieves identity providers from Dremio.

```
GET https://connect.mindcloud.co/v1/universal/dremio/latest/actions/list-identity-providers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dremio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dremio/latest/actions/list-identity-providers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dremio/latest/actions/list-identity-providers?${params}`, {
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
      "enterprise": [
        {}
      ],
      "local": {},
      "social": [
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
| `enterprise` | array<object> |  |
| `local` | object |  |
| `social` | array<object> |  |

## Native endpoint

Through the native Dremio API, this operation is `GET /identity-providers` (base URL `https://api.dremio.cloud/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-identity-providers.md) for the provider-specific parameters and requirements.

