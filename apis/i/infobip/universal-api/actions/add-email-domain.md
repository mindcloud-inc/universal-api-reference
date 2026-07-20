# Infobip: Add Email Domain



```
POST https://connect.mindcloud.co/v1/universal/infobip/latest/actions/add-email-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infobip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/infobip/latest/actions/add-email-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domainName": "Ava Chen",
  "targetedDailyTraffic": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/infobip/latest/actions/add-email-domain', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domainName": "Ava Chen",
    "targetedDailyTraffic": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domainName` | string | yes | Unique name for the domain. |
| `dkimKeyLength` | string | no | Value for DKIM key length. |
| `targetedDailyTraffic` | number | yes | Targeted daily traffic. |
| `applicationId` | string | no | Required for application use in a send request for outbound traffic. Returned in notification events. |
| `entityId` | string | no | Required for entity use in a send request for outbound traffic. Returned in notification events. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "blocked": true,
      "blocklistConfigurationLevel": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dnsRecords": {
        "expectedValue": "string",
        "name": "Ava Chen",
        "recordType": "string",
        "verified": true
      },
      "domainId": 1,
      "domainName": "Ava Chen",
      "tracking": {
        "clicks": true,
        "opens": true,
        "unsubscribe": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `blocked` | boolean |  |
| `blocklistConfigurationLevel` | string |  |
| `createdAt` | date |  |
| `dnsRecords` | array<object> |  |
| `dnsRecords.expectedValue` | string |  |
| `dnsRecords.name` | string |  |
| `dnsRecords.recordType` | string |  |
| `dnsRecords.verified` | boolean |  |
| `domainId` | number |  |
| `domainName` | string |  |
| `tracking` | object |  |
| `tracking.clicks` | boolean |  |
| `tracking.opens` | boolean |  |
| `tracking.unsubscribe` | boolean |  |

## Native endpoint

Through the native Infobip API, this operation is `POST /email/1/domains` (base URL `https://rkpzwe.api.infobip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-email-domain.md) for the provider-specific parameters and requirements.

