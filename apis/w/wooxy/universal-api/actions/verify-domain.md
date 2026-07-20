# Wooxy: Verify Domain

Verifies an existing domain in Wooxy.

```
PUT https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/verify-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wooxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/verify-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/verify-domain', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domainId` | string | no | The Wooxy domain ID. Use this or Domain. Example: `69d68b03cab91f1ed601af02`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domain` | string | no | The registered domain name. Use this or Domain ID. Example: `stage3-20260408.example.com`. |

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
      "resolve": [
        {}
      ],
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
| `resolve` | array<object> |  |
| `result` | boolean |  |

## Native endpoint

Through the native Wooxy API, this operation is `POST v3/domain/verify` (base URL `https://api.wooxy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-domain.md) for the provider-specific parameters and requirements.

