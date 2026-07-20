# Snapchat Ads: Fetch Ad Squads by IDs

Retrieves ad squads from Snapchat Ads by ad squad IDs.

```
GET https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/fetch-ad-squads-by-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snapchat Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/fetch-ad-squads-by-ids?connectionId=$CONNECTION_ID&adAccountId=string&adSquadIds=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "adAccountId": "string",
  "adSquadIds": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/fetch-ad-squads-by-ids?${params}`, {
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
| `adSquadIds` | list<string> | yes | An array of Snapchat Ad Squad IDs to fetch. |

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

Through the native Snapchat Ads API, this operation is `POST /adaccounts/:adAccountId/get_adsquads_by_ids` (base URL `https://adsapi.snapchat.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-ad-squads-by-ids.md) for the provider-specific parameters and requirements.

