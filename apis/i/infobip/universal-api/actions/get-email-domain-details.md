# Infobip: Get Email Domain Details



```
GET https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get-email-domain-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infobip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get-email-domain-details?connectionId=$CONNECTION_ID&domainName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domainName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get-email-domain-details?${params}`, {
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
| `domainName` | string | yes | Domain for which the details need to be viewed. |

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

Through the native Infobip API, this operation is `GET /email/1/domains/{domainName}` (base URL `https://rkpzwe.api.infobip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-domain-details.md) for the provider-specific parameters and requirements.

