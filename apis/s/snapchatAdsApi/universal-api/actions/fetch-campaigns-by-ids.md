# Snapchat Ads: Fetch Campaigns by IDs

Retrieves campaigns from Snapchat Ads by campaign IDs.

```
GET https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/fetch-campaigns-by-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snapchat Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/fetch-campaigns-by-ids?connectionId=$CONNECTION_ID&adAccountId=string&campaignIds=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "adAccountId": "string",
  "campaignIds": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/fetch-campaigns-by-ids?${params}`, {
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
| `adAccountId` | string | yes | The Snapchat Ad Account ID that owns the campaigns. |
| `campaignIds` | list<string> | yes | An array of Snapchat Campaign IDs to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaigns": [
        {
          "campaign": {
            "id": "string",
            "name": "Ava Chen",
            "objective": "string",
            "status": "string"
          }
        }
      ],
      "request_id": "string",
      "request_status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaigns[].campaign.id` | string |  |
| `campaigns[].campaign.name` | string |  |
| `campaigns[].campaign.objective` | string |  |
| `campaigns[].campaign.status` | string |  |
| `request_id` | string |  |
| `request_status` | string |  |

## Native endpoint

Through the native Snapchat Ads API, this operation is `POST /adaccounts/:adAccountId/get_campaigns_by_ids` (base URL `https://adsapi.snapchat.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-campaigns-by-ids.md) for the provider-specific parameters and requirements.

