# Zoho Connect: Get All Networks

Retrieves all networks from Zoho Connect.

```
GET https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/get-all-networks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/get-all-networks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/get-all-networks?${params}`, {
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
      "id": "string",
      "isDefault": "string",
      "logoUrl": "https://example.com",
      "name": "Ava Chen",
      "soid": "string",
      "url": "https://example.com",
      "zoid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `isDefault` | string |  |
| `logoUrl` | string |  |
| `name` | string |  |
| `soid` | string |  |
| `url` | string |  |
| `zoid` | string |  |

## Native endpoint

Through the native Zoho Connect API, this operation is `GET /pulse/api/allScopes` (base URL `https://connect.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-networks.md) for the provider-specific parameters and requirements.

