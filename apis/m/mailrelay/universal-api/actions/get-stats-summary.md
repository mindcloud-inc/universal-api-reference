# Mailrelay: Get Stats Summary

Retrieves account stats summary from Mailrelay.

```
GET https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/get-stats-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailrelay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/get-stats-summary?connectionId=$CONNECTION_ID&endTime=2026-04-08%2023%3A59%3A59&startTime=2026-04-06%2000%3A00%3A00" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "endTime": "2026-04-08 23:59:59",
  "startTime": "2026-04-06 00:00:00"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailrelay/latest/actions/get-stats-summary?${params}`, {
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
| `endTime` | string | yes | End time in `YYYY-MM-DD HH:MM:SS` format. Example: `2026-04-08 23:59:59`. |
| `startTime` | string | yes | Start time in `YYYY-MM-DD HH:MM:SS` format. Example: `2026-04-06 00:00:00`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bouncedEmails": 1,
      "clicks": 1,
      "deliveredEmails": 1,
      "impressions": 1,
      "processedEmails": 1,
      "sentEmails": 1,
      "softBouncedEmails": 1,
      "uniqueClicks": 1,
      "uniqueImpressions": 1,
      "unsubscribeEvents": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bouncedEmails` | number |  |
| `clicks` | number |  |
| `deliveredEmails` | number |  |
| `impressions` | number |  |
| `processedEmails` | number |  |
| `sentEmails` | number |  |
| `softBouncedEmails` | number |  |
| `uniqueClicks` | number |  |
| `uniqueImpressions` | number |  |
| `unsubscribeEvents` | number |  |

## Native endpoint

Through the native Mailrelay API, this operation is `GET stats` (base URL `https://{{credentials.accountDomain}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stats-summary.md) for the provider-specific parameters and requirements.

