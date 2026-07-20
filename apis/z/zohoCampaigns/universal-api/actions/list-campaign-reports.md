# Zoho Campaigns: List Campaign Reports

Retrieves campaign reports from Zoho Campaigns.

```
GET https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/list-campaign-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Campaigns `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/list-campaign-reports?connectionId=$CONNECTION_ID&campaignKey=f70c4878c4a47169407e63917ad24497" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignKey": "f70c4878c4a47169407e63917ad24497"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/list-campaign-reports?${params}`, {
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
| `campaignKey` | string | yes | Campaign key from a recent-campaign response. Example: `f70c4878c4a47169407e63917ad24497`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bounces": "string",
      "clicks": "string",
      "delivered": "string",
      "forwards": "string",
      "opens": "string",
      "sent": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bounces` | string | Bounce count returned by Zoho for the campaign. |
| `clicks` | string | Click count returned by Zoho for the campaign. |
| `delivered` | string | Delivered count returned by Zoho for the campaign. |
| `forwards` | string | Forward count returned by Zoho for the campaign. |
| `opens` | string | Open count returned by Zoho for the campaign. |
| `sent` | string | Sent count returned by Zoho for the campaign. |

## Native endpoint

Through the native Zoho Campaigns API, this operation is `GET /campaignreports` (base URL `https://campaigns.zoho.com/api/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaign-reports.md) for the provider-specific parameters and requirements.

