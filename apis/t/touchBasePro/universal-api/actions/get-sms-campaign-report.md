# TouchBasePro: Get SMS Campaign Report

Retrieves an SMS campaign report from TouchBasePro.

```
GET https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-sms-campaign-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TouchBasePro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-sms-campaign-report?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-sms-campaign-report?${params}`, {
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
      "bounced": [
        [
          {}
        ]
      ],
      "delivered": [
        [
          {}
        ]
      ],
      "name": "Ava Chen",
      "recipients": [
        [
          "string"
        ]
      ],
      "replies": [
        [
          {}
        ]
      ],
      "status": "string",
      "totalBounced": 1,
      "totalDelivered": 1,
      "totalRecipients": 1,
      "totalReplies": 1,
      "totalUnsubscribed": 1,
      "unsubscribed": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bounced[]` | array<object> |  |
| `bounced[].date` | date |  |
| `bounced[].number` | string |  |
| `delivered[]` | array<object> |  |
| `delivered[].date` | date |  |
| `delivered[].number` | string |  |
| `name` | string |  |
| `recipients[]` | array<string> |  |
| `replies[]` | array<object> |  |
| `replies[].date` | date |  |
| `replies[].message` | string |  |
| `replies[].number` | string |  |
| `status` | string |  |
| `totalBounced` | number |  |
| `totalDelivered` | number |  |
| `totalRecipients` | number |  |
| `totalReplies` | number |  |
| `totalUnsubscribed` | number |  |
| `unsubscribed[]` | array<object> |  |
| `unsubscribed[].date` | date |  |
| `unsubscribed[].number` | string |  |

## Native endpoint

Through the native TouchBasePro API, this operation is `GET /sms/campaigns/{campaignId}/report` (base URL `https://api.touchbasepro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sms-campaign-report.md) for the provider-specific parameters and requirements.

