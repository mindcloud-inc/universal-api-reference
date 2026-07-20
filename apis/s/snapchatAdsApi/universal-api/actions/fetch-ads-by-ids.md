# Snapchat Ads: Fetch Ads by IDs

Retrieves ads from Snapchat Ads by ad IDs.

```
GET https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/fetch-ads-by-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snapchat Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/fetch-ads-by-ids?connectionId=$CONNECTION_ID&adAccountId=string&adIds=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "adAccountId": "string",
  "adIds": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/fetch-ads-by-ids?${params}`, {
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
| `adAccountId` | string | yes | The Snapchat Ad Account ID that owns the ads. |
| `adIds` | list<string> | yes | An array of Snapchat Ad IDs to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ads": [
        {
          "ad": {
            "id": "string",
            "name": "Ava Chen",
            "review_status": "string",
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
| `ads[].ad.id` | string |  |
| `ads[].ad.name` | string |  |
| `ads[].ad.review_status` | string |  |
| `ads[].ad.status` | string |  |
| `request_id` | string |  |
| `request_status` | string |  |

## Native endpoint

Through the native Snapchat Ads API, this operation is `POST /adaccounts/:adAccountId/get_ads_by_ids` (base URL `https://adsapi.snapchat.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-ads-by-ids.md) for the provider-specific parameters and requirements.

