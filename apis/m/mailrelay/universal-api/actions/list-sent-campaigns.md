# Mailrelay: List Sent Campaigns

Retrieves sent campaigns from your Mailrelay account.

```
GET https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/list-sent-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailrelay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/list-sent-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/list-sent-campaigns?${params}`, {
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

Through the native Mailrelay API, this operation is `GET sent_campaigns` (base URL `https://{{credentials.accountDomain}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sent-campaigns.md) for the provider-specific parameters and requirements.

