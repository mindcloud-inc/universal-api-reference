# SuperSend: Get Domain

Retrieves a domain from SuperSend.

```
GET https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-domain?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-domain?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeSenderCount": 1,
      "autoRenew": true,
      "cancelAtPeriodEnd": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dmarcEmail": "ava@example.com",
      "dnsProvider": "string",
      "dnsRecords": {
        "dkim": {},
        "dmarc": {},
        "mx": [
          [
            {}
          ]
        ],
        "spf": {}
      },
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "forwardingAddress": "string",
      "health": {
        "blacklistProviders": [
          [
            "string"
          ]
        ],
        "blacklistReason": "string",
        "dkimValid": true,
        "dmarcValid": true,
        "dnsValid": true,
        "errors": [
          [
            "string"
          ]
        ],
        "isActive": true,
        "isBlacklisted": true,
        "lastCheck": "2026-05-07T12:00:00.000Z",
        "mxValid": true,
        "records": {
          "dkim": "string",
          "dmarc": "string",
          "mx": [
            [
              "string"
            ]
          ],
          "nameservers": [
            [
              "Ava Chen"
            ]
          ],
          "spf": "string"
        },
        "spfValid": true,
        "warnings": [
          [
            "string"
          ]
        ]
      },
      "id": "string",
      "managed": "string",
      "name": "Ava Chen",
      "object": "string",
      "provider": "string",
      "registrar": "string",
      "senders": [
        {
          "disabled": true,
          "email": "ava@example.com",
          "healthScore": 1,
          "id": "string",
          "sendAs": "string",
          "status": "string",
          "warm": true,
          "warmingStage": 1
        }
      ],
      "status": "string",
      "team": {
        "id": "string",
        "name": "Ava Chen"
      },
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeSenderCount` | number |  |
| `autoRenew` | boolean |  |
| `cancelAtPeriodEnd` | boolean |  |
| `createdAt` | date |  |
| `dmarcEmail` | string |  |
| `dnsProvider` | string |  |
| `dnsRecords.dkim` | object |  |
| `dnsRecords.dmarc` | object |  |
| `dnsRecords.mx[]` | array<object> |  |
| `dnsRecords.spf` | object |  |
| `expiresAt` | date |  |
| `forwardingAddress` | string |  |
| `health.blacklistProviders[]` | array<string> |  |
| `health.blacklistReason` | string |  |
| `health.dkimValid` | boolean |  |
| `health.dmarcValid` | boolean |  |
| `health.dnsValid` | boolean |  |
| `health.errors[]` | array<string> |  |
| `health.isActive` | boolean |  |
| `health.isBlacklisted` | boolean |  |
| `health.lastCheck` | date |  |
| `health.mxValid` | boolean |  |
| `health.records.dkim` | string |  |
| `health.records.dmarc` | string |  |
| `health.records.mx[]` | array<string> |  |
| `health.records.nameservers[]` | array<string> |  |
| `health.records.spf` | string |  |
| `health.spfValid` | boolean |  |
| `health.warnings[]` | array<string> |  |
| `id` | string |  |
| `managed` | string |  |
| `name` | string |  |
| `object` | string |  |
| `provider` | string |  |
| `registrar` | string |  |
| `senders[].disabled` | boolean |  |
| `senders[].email` | string |  |
| `senders[].healthScore` | number |  |
| `senders[].id` | string |  |
| `senders[].sendAs` | string |  |
| `senders[].status` | string |  |
| `senders[].warm` | boolean |  |
| `senders[].warmingStage` | number |  |
| `status` | string |  |
| `team.id` | string |  |
| `team.name` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native SuperSend API, this operation is `GET /domains/{id}` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domain.md) for the provider-specific parameters and requirements.

