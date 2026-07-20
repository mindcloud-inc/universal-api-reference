# Pinata: List Gateways

Retrieves gateways from Pinata for the current account.

```
GET https://connect.mindcloud.co/v1/universal/pinata/latest/actions/list-gateways
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinata/latest/actions/list-gateways?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinata/latest/actions/list-gateways?${params}`, {
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "custom_domains": [
        "string"
      ],
      "domain": "string",
      "id": "string",
      "restrict": true,
      "settings": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Creation timestamp. |
| `custom_domains` | array<string> | Attached custom domains. |
| `domain` | string | Gateway domain. |
| `id` | string | Gateway ID. |
| `restrict` | boolean | Whether the gateway is restricted. |
| `settings` | object | Gateway settings object. |

## Native endpoint

Through the native Pinata API, this operation is `GET /v3/gateways` (base URL `https://api.pinata.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-gateways.md) for the provider-specific parameters and requirements.

