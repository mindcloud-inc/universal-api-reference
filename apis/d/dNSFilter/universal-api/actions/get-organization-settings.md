# DNSFilter: Get Organization Settings



```
GET https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/get-organization-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DNSFilter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/get-organization-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/get-organization-settings?${params}`, {
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
      "connection_method": "string",
      "diagnostics_level": "string",
      "fail_over_method": "string",
      "filtering_method": "string",
      "id": 1,
      "name": "Ava Chen",
      "privacy_mode": "string",
      "user_agents_auto_update": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `connection_method` | string |  |
| `diagnostics_level` | string |  |
| `fail_over_method` | string |  |
| `filtering_method` | string |  |
| `id` | number |  |
| `name` | string |  |
| `privacy_mode` | string |  |
| `user_agents_auto_update` | boolean |  |

## Native endpoint

Through the native DNSFilter API, this operation is `GET /v1/organizations/settings` (base URL `https://api.dnsfilter.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-settings.md) for the provider-specific parameters and requirements.

