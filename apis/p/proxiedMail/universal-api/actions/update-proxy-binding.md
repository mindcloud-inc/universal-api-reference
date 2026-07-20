# ProxiedMail: Update Proxy Binding



```
PUT https://connect.mindcloud.co/v1/universal/proxiedMail/latest/actions/update-proxy-binding
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProxiedMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/proxiedMail/latest/actions/update-proxy-binding" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "proxyBindingId": "A8AEDDF2-F100-0000-00000BAE"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/proxiedMail/latest/actions/update-proxy-binding', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "proxyBindingId": "A8AEDDF2-F100-0000-00000BAE"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `proxyBindingId` | string | yes | Example: `A8AEDDF2-F100-0000-00000BAE`. |
| `proxyAddress` | string | no | Example: `news-207437@proxiedmail.com`. |
| `realAddresses` | list<string> | no | Accepts multiple values as an array. Example: `apps@mindcloud.co`. |
| `description` | string | no | Example: `Proxy binding description`. |
| `callbackUrl` | string | no | Example: `https://example.com/webhook`. |
| `isBrowsable` | boolean | no |  |

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
          "stage3RecipientA20260330@int": {
            "proxiedmail": {
              "com": {
                "confirmationRequestShown": true,
                "isEnabled": true,
                "isVerified": true,
                "verificationType": 1
              }
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
| `attributes.realAddresses.stage3RecipientA20260330@int.proxiedmail.com.confirmationRequestShown` | boolean |  |
| `attributes.realAddresses.stage3RecipientA20260330@int.proxiedmail.com.isEnabled` | boolean |  |
| `attributes.realAddresses.stage3RecipientA20260330@int.proxiedmail.com.isVerified` | boolean |  |
| `attributes.realAddresses.stage3RecipientA20260330@int.proxiedmail.com.verificationType` | number |  |
| `attributes.receivedEmails` | number |  |
| `attributes.type` | number |  |
| `attributes.updatedAt` | string |  |
| `attributes.wildcardAutoCreateOn` | object |  |
| `id` | string |  |
| `relationships.user.data.id` | string |  |
| `relationships.user.data.type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native ProxiedMail API, this operation is `PATCH /proxy-bindings/:proxyBindingId` (base URL `https://proxiedmail.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-proxy-binding.md) for the provider-specific parameters and requirements.

