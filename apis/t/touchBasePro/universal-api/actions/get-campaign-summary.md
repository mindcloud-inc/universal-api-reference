# TouchBasePro: Get Campaign Summary

Retrieves a campaign summary from TouchBasePro.

```
GET https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-campaign-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TouchBasePro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-campaign-summary?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/get-campaign-summary?${params}`, {
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
      "bounced": 1,
      "clicks": 1,
      "forwards": 1,
      "likes": 1,
      "mentions": 1,
      "recipients": 1,
      "spamComplaints": 1,
      "totalOpened": 1,
      "uniqueOpened": 1,
      "unsubscribed": 1,
      "webVersionTextUrl": "https://example.com",
      "webVersionUrl": "https://example.com",
      "worldviewUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bounced` | number |  |
| `clicks` | number |  |
| `forwards` | number |  |
| `likes` | number |  |
| `mentions` | number |  |
| `recipients` | number |  |
| `spamComplaints` | number |  |
| `totalOpened` | number |  |
| `uniqueOpened` | number |  |
| `unsubscribed` | number |  |
| `webVersionTextUrl` | string |  |
| `webVersionUrl` | string |  |
| `worldviewUrl` | string |  |

## Native endpoint

Through the native TouchBasePro API, this operation is `GET /email/campaigns/{campaignId}/summary` (base URL `https://api.touchbasepro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-summary.md) for the provider-specific parameters and requirements.

