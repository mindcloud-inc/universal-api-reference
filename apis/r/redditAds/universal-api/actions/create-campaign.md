# Reddit Lead Ads: Create Campaign

Creates a campaign in Reddit Ads.

```
POST https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/create-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reddit Lead Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "adAccountId": "string",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/create-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "adAccountId": "string",
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `adAccountId` | string | yes | The ID of the ad account to create the campaign under. |
| `data` | object | yes | JSON request body from the Reddit Ads API spec. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Campaign identifier. |
| `name` | string | Campaign name. |
| `status` | string | Campaign status. |

## Native endpoint

Through the native Reddit Lead Ads API, this operation is `POST /ad_accounts/{ad_account_id}/campaigns` (base URL `https://ads-api.reddit.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign.md) for the provider-specific parameters and requirements.

