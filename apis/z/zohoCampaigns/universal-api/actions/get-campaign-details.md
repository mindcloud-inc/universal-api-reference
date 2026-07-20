# Zoho Campaigns: Get Campaign Details

Retrieves campaign details from Zoho Campaigns.

```
GET https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/get-campaign-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Campaigns `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/get-campaign-details?connectionId=$CONNECTION_ID&campaignKey=f70c4878c4a47169407e63917ad24497" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignKey": "f70c4878c4a47169407e63917ad24497"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/get-campaign-details?${params}`, {
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
| `campaignType` | string | no | Campaign type for the selected campaign. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "associatedMailingLists": [
        {}
      ],
      "campaignDetails": [
        {}
      ],
      "campaignStatus": "string",
      "code": "string",
      "segmentsInfo": [
        {}
      ],
      "status": "string",
      "totalSubscribersCount": 1,
      "url": "https://example.com",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `associatedMailingLists` | array<object> | Mailing lists associated with the campaign. |
| `campaignDetails` | array<object> | Detailed Zoho campaign payload. |
| `campaignStatus` | string | Campaign status. |
| `code` | string | Provider response code. |
| `segmentsInfo` | array<object> | Segment information for the campaign. |
| `status` | string | Provider status. |
| `totalSubscribersCount` | number | Total subscribers currently associated with the campaign. |
| `url` | string | Provider endpoint identifier. |
| `version` | string | Provider API version. |

## Native endpoint

Through the native Zoho Campaigns API, this operation is `GET /getcampaigndetails` (base URL `https://campaigns.zoho.com/api/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-details.md) for the provider-specific parameters and requirements.

