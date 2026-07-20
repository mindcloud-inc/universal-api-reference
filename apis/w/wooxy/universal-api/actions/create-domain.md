# Wooxy: Create Domain

Creates a new domain in Wooxy.

```
POST https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/create-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wooxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/create-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domain": "stage3-20260408.example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/create-domain', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domain": "stage3-20260408.example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domain` | string | yes | The domain to create. Must be a valid domain name. Example: `stage3-20260408.example.com`. |
| `webHookUri` | string | no | Optional webhook URL to receive the domain-created callback. Example: `https://example.com/webhooks/wooxy-domain`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "createdAt": "string",
        "dnsRecords": [
          {}
        ],
        "dnsSubdomain": "string",
        "dnsVerified": true,
        "domain": "string",
        "domainId": "string",
        "emailVerified": true,
        "id": "string",
        "warmupDay": 1,
        "warmupStatus": 1
      },
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.createdAt` | string |  |
| `data.dnsRecords` | array<object> |  |
| `data.dnsSubdomain` | string |  |
| `data.dnsVerified` | boolean |  |
| `data.domain` | string |  |
| `data.domainId` | string |  |
| `data.emailVerified` | boolean |  |
| `data.id` | string |  |
| `data.warmupDay` | number |  |
| `data.warmupStatus` | number |  |
| `result` | boolean |  |

## Native endpoint

Through the native Wooxy API, this operation is `POST v3/domain/create` (base URL `https://api.wooxy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-domain.md) for the provider-specific parameters and requirements.

