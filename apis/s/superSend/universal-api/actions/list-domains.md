# SuperSend: List Domains

Retrieves domains from SuperSend.

```
GET https://connect.mindcloud.co/v1/universal/superSend/latest/actions/list-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/list-domains?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superSend/latest/actions/list-domains?${params}`, {
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
| `teamId` | string | no |  |
| `status` | string | no | Allowed values: pending, purchasing, purchased, setting_up, active, purchase_failed, setup_failed, inactive, expired, cancelled. |
| `managed` | string | no | Allowed values: internal, external. |
| `search` | string | no |  |
| `limit` | number | no | Default: 50. Range: 1 to 100. |
| `offset` | number | no | Default: 0. Range: 0 to inf. |

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
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "health": {
        "dkimValid": true,
        "dmarcValid": true,
        "dnsValid": true,
        "isActive": true,
        "isBlacklisted": true,
        "lastCheck": "2026-05-07T12:00:00.000Z",
        "mxValid": true,
        "spfValid": true
      },
      "id": "string",
      "managed": "string",
      "name": "Ava Chen",
      "object": "string",
      "provider": "string",
      "registrar": "string",
      "status": "string",
      "teamId": "string",
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
| `expiresAt` | date |  |
| `health.dkimValid` | boolean |  |
| `health.dmarcValid` | boolean |  |
| `health.dnsValid` | boolean |  |
| `health.isActive` | boolean |  |
| `health.isBlacklisted` | boolean |  |
| `health.lastCheck` | date |  |
| `health.mxValid` | boolean |  |
| `health.spfValid` | boolean |  |
| `id` | string |  |
| `managed` | string |  |
| `name` | string |  |
| `object` | string |  |
| `provider` | string |  |
| `registrar` | string |  |
| `status` | string |  |
| `teamId` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native SuperSend API, this operation is `GET /domains` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-domains.md) for the provider-specific parameters and requirements.

