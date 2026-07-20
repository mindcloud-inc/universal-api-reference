# Sendloop: Get Campaign



```
GET https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/get-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendloop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/get-campaign?connectionId=$CONNECTION_ID&campaignId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/get-campaign?${params}`, {
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
| `campaignId` | number | yes | Target campaign ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignID": 1,
      "campaignName": "Ava Chen",
      "campaignStatus": "string",
      "fromEmail": "ava@example.com",
      "fromName": "Ava Chen",
      "lists": [
        1
      ],
      "replyToEmail": "ava@example.com",
      "replyToName": "Ava Chen",
      "scheduleType": "string",
      "subject": "string",
      "totalClicks": 1,
      "totalFailed": 1,
      "totalOpens": 1,
      "totalRecipients": 1,
      "totalSent": 1,
      "totalUnsubscriptions": 1,
      "uniqueClicks": 1,
      "uniqueOpens": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignID` | number |  |
| `campaignName` | string |  |
| `campaignStatus` | string |  |
| `fromEmail` | string |  |
| `fromName` | string |  |
| `lists` | array<number> |  |
| `replyToEmail` | string |  |
| `replyToName` | string |  |
| `scheduleType` | string |  |
| `subject` | string |  |
| `totalClicks` | number |  |
| `totalFailed` | number |  |
| `totalOpens` | number |  |
| `totalRecipients` | number |  |
| `totalSent` | number |  |
| `totalUnsubscriptions` | number |  |
| `uniqueClicks` | number |  |
| `uniqueOpens` | number |  |

## Native endpoint

Through the native Sendloop API, this operation is `POST /campaign.get/json` (base URL `https://{{credentials.subdomain}}.sendloop.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign.md) for the provider-specific parameters and requirements.

