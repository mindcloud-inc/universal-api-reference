# Zoho Campaigns: List Recently Sent Campaigns

Retrieves recently sent campaigns from Zoho Campaigns.

```
GET https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/list-recently-sent-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Campaigns `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/list-recently-sent-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/list-recently-sent-campaigns?${params}`, {
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
      "campaignKey": "string",
      "campaignName": "Ava Chen",
      "createdTime": "string",
      "sentTime": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignKey` | string | Unique key of the recently sent campaign. |
| `campaignName` | string | Name of the recently sent campaign. |
| `createdTime` | string | Campaign creation timestamp in epoch milliseconds. |
| `sentTime` | string | Sent timestamp in epoch milliseconds for the campaign row. |

## Native endpoint

Through the native Zoho Campaigns API, this operation is `GET /recentsentcampaigns` (base URL `https://campaigns.zoho.com/api/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recently-sent-campaigns.md) for the provider-specific parameters and requirements.

