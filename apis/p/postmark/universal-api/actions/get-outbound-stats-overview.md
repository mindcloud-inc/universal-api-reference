# Postmark: Get Outbound Stats Overview

Retrieves outbound stats overview from Postmark.

```
GET https://connect.mindcloud.co/v1/universal/postmark/latest/actions/get-outbound-stats-overview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postmark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postmark/latest/actions/get-outbound-stats-overview?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postmark/latest/actions/get-outbound-stats-overview?${params}`, {
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
      "Bounced": 1,
      "BounceRate": 1,
      "Opens": 1,
      "Sent": 1,
      "SMTPAPIErrors": 1,
      "SpamComplaints": 1,
      "TotalClicks": 1,
      "UniqueOpens": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Bounced` | number |  |
| `BounceRate` | number |  |
| `Opens` | number |  |
| `Sent` | number |  |
| `SMTPAPIErrors` | number |  |
| `SpamComplaints` | number |  |
| `TotalClicks` | number |  |
| `UniqueOpens` | number |  |

## Native endpoint

Through the native Postmark API, this operation is `GET /stats/outbound` (base URL `https://api.postmarkapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-outbound-stats-overview.md) for the provider-specific parameters and requirements.

