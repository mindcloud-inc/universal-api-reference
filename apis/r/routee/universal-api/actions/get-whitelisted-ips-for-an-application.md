# Routee: Get whitelisted IP's for an application

Retrieves whitelisted IPs for an application from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/get-whitelisted-ips-for-an-application
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/get-whitelisted-ips-for-an-application?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/get-whitelisted-ips-for-an-application?${params}`, {
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
      "whitelistedIps": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `whitelistedIps[]` | array<string> |  |

## Native endpoint

Through the native Routee API, this operation is `GET /security/whitelist` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-whitelisted-ips-for-an-application.md) for the provider-specific parameters and requirements.

