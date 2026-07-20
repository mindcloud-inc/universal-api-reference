# ProxiedMail: List Proxy Bindings



```
GET https://connect.mindcloud.co/v1/universal/proxiedMail/latest/actions/list-proxy-bindings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProxiedMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proxiedMail/latest/actions/list-proxy-bindings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proxiedMail/latest/actions/list-proxy-bindings?${params}`, {
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
      "attributes": {
        "callbackUrl": "https://example.com",
        "createdAt": "string",
        "deliveryMethod": 1,
        "description": "string",
        "isBrowsable": true,
        "proxyAddress": "string",
        "realAddresses": {
          "apps@mindcloud": {
            "co": {
              "confirmationRequestShown": true,
              "isEnabled": true,
              "isVerified": true,
              "verificationType": 1
            }
          }
        },
        "receivedEmails": 1,
        "type": 1,
        "updatedAt": "string",
        "wildcardAutoCreateOn": {}
      },
      "id": "string",
      "relationships": {
        "user": {
          "data": {
            "id": "string",
            "type": "string"
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.callbackUrl` | string |  |
| `attributes.createdAt` | string |  |
| `attributes.deliveryMethod` | number |  |
| `attributes.description` | string |  |
| `attributes.isBrowsable` | boolean |  |
| `attributes.proxyAddress` | string |  |
| `attributes.realAddresses.apps@mindcloud.co.confirmationRequestShown` | boolean |  |
| `attributes.realAddresses.apps@mindcloud.co.isEnabled` | boolean |  |
| `attributes.realAddresses.apps@mindcloud.co.isVerified` | boolean |  |
| `attributes.realAddresses.apps@mindcloud.co.verificationType` | number |  |
| `attributes.receivedEmails` | number |  |
| `attributes.type` | number |  |
| `attributes.updatedAt` | string |  |
| `attributes.wildcardAutoCreateOn` | object |  |
| `id` | string |  |
| `relationships.user.data.id` | string |  |
| `relationships.user.data.type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native ProxiedMail API, this operation is `GET /proxy-bindings` (base URL `https://proxiedmail.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-proxy-bindings.md) for the provider-specific parameters and requirements.

