# Zoho Campaigns: List Recent Campaigns

Retrieves recent campaigns from Zoho Campaigns.

```
GET https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/list-recent-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Campaigns `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/list-recent-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/list-recent-campaigns?${params}`, {
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
| `sort` | string | no | Sort order for the recent campaigns list. One of: `0`, `1`. |
| `fromIndex` | number | no | Starting index for the campaign list. Example: `1`. |
| `range` | number | no | Maximum number of campaigns to return. Example: `5`. |
| `status` | string | no | Campaign status filter. One of: `0`, `1`, `10`, `11`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignId": "string",
      "campaignKey": "string",
      "campaignName": "Ava Chen",
      "campaignPreview": "string",
      "campaignStatus": "string",
      "campaigntype": "string",
      "createdDateString": "string",
      "createdTimeGmt": "string",
      "folderId": "string",
      "fromEmail": "ava@example.com",
      "isHybrid": "string",
      "replyTo": "string",
      "subject": "string",
      "zuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignId` | string | Zoho campaign identifier. |
| `campaignKey` | string | Zoho campaign key. |
| `campaignName` | string | Campaign name. |
| `campaignPreview` | string | Campaign preview snippet. |
| `campaignStatus` | string | Campaign status. |
| `campaigntype` | string | Campaign type. |
| `createdDateString` | string | Campaign creation timestamp. |
| `createdTimeGmt` | string | Creation time in GMT. |
| `folderId` | string | Folder identifier. |
| `fromEmail` | string | Sender email. |
| `isHybrid` | string | Hybrid-campaign flag. |
| `replyTo` | string | Reply-to email. |
| `subject` | string | Email subject. |
| `zuid` | string | Zoho user identifier. |

## Native endpoint

Through the native Zoho Campaigns API, this operation is `GET /recentcampaigns` (base URL `https://campaigns.zoho.com/api/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recent-campaigns.md) for the provider-specific parameters and requirements.

