# Infobip: Update Email Domain Tracking Events



```
PUT https://connect.mindcloud.co/v1/universal/infobip/latest/actions/update-email-domain-tracking-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infobip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/infobip/latest/actions/update-email-domain-tracking-events" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domainName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/infobip/latest/actions/update-email-domain-tracking-events', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domainName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domainName` | string | yes | Domain for which the tracking events need to be updated. |
| `open` | boolean | no | Boolean value corresponding to whether opens for a message needs to be tracked or not. |
| `clicks` | boolean | no | Boolean value corresponding to whether clicks for a message needs to be tracked or not. |
| `unsubscribe` | boolean | no | Boolean value corresponding to whether unsubscribe for a message needs to be tracked or not. |

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

Through the native Infobip API, this operation is `PUT /email/1/domains/{domainName}/tracking` (base URL `https://rkpzwe.api.infobip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-email-domain-tracking-events.md) for the provider-specific parameters and requirements.

