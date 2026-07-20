# TouchBasePro: Get SMS Campaign

Retrieves an SMS campaign from TouchBasePro.

```
GET https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-sms-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TouchBasePro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-sms-campaign?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-sms-campaign?${params}`, {
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
      "campaignId": 1,
      "content": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "deliveryDate": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "repliesToEmail": "ava@example.com",
      "repliesToMobile": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignId` | number |  |
| `content` | string |  |
| `date` | date |  |
| `deliveryDate` | date |  |
| `name` | string |  |
| `repliesToEmail` | string |  |
| `repliesToMobile` | string |  |
| `status` | string |  |

## Native endpoint

Through the native TouchBasePro API, this operation is `GET /sms/campaigns/{campaignId}` (base URL `https://api.touchbasepro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sms-campaign.md) for the provider-specific parameters and requirements.

