# Mailrelay: Get Sent Campaign

Retrieves a sent campaign from Mailrelay.

```
GET https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/get-sent-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailrelay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/get-sent-campaign?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/get-sent-campaign?${params}`, {
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
| `id` | number | yes | The Mailrelay sent campaign ID. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bouncedEmailsCount": 1,
      "clicksCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deliveredEmailsCount": 1,
      "finishedAt": "2026-05-07T12:00:00.000Z",
      "html": "string",
      "id": 1,
      "impressionsCount": 1,
      "previewText": "string",
      "processedEmailsCount": 1,
      "scheduledAt": "2026-05-07T12:00:00.000Z",
      "senderId": 1,
      "sentEmailsCount": 1,
      "softBouncedEmailsCount": 1,
      "status": "string",
      "subject": "string",
      "uniqueClicksCount": 1,
      "uniqueImpressionsCount": 1,
      "unsubscribeEventsCount": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bouncedEmailsCount` | number |  |
| `clicksCount` | number |  |
| `createdAt` | date |  |
| `deliveredEmailsCount` | number |  |
| `finishedAt` | date |  |
| `html` | string |  |
| `id` | number |  |
| `impressionsCount` | number |  |
| `previewText` | string |  |
| `processedEmailsCount` | number |  |
| `scheduledAt` | date |  |
| `senderId` | number |  |
| `sentEmailsCount` | number |  |
| `softBouncedEmailsCount` | number |  |
| `status` | string |  |
| `subject` | string |  |
| `uniqueClicksCount` | number |  |
| `uniqueImpressionsCount` | number |  |
| `unsubscribeEventsCount` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Mailrelay API, this operation is `GET sent_campaigns/:id` (base URL `https://{{credentials.accountDomain}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sent-campaign.md) for the provider-specific parameters and requirements.

