# Snapchat Ads: List Ad Squads by Ad Account

Retrieves ad squads from Snapchat Ads by ad account.

```
GET https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/list-ad-squads-by-ad-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snapchat Ads `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/list-ad-squads-by-ad-account?connectionId=$CONNECTION_ID&limit=25&offset=0&adAccountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "adAccountId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/list-ad-squads-by-ad-account?${params}`, {
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
| `adAccountId` | string | yes | The Snapchat Ad Account ID that owns the ad squads. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adsquads": [
        {
          "adsquad": {
            "id": "string",
            "name": "Ava Chen",
            "optimization_goal": "string",
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
| `adsquads[].adsquad.id` | string |  |
| `adsquads[].adsquad.name` | string |  |
| `adsquads[].adsquad.optimization_goal` | string |  |
| `adsquads[].adsquad.status` | string |  |
| `request_id` | string |  |
| `request_status` | string |  |

## Native endpoint

Through the native Snapchat Ads API, this operation is `GET /adaccounts/:adAccountId/adsquads` (base URL `https://adsapi.snapchat.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-ad-squads-by-ad-account.md) for the provider-specific parameters and requirements.

