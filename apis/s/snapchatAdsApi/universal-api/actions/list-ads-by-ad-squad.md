# Snapchat Ads: List Ads by Ad Squad

Retrieves ads from Snapchat Ads by ad squad.

```
GET https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/list-ads-by-ad-squad
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snapchat Ads `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/list-ads-by-ad-squad?connectionId=$CONNECTION_ID&limit=25&offset=0&adSquadId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "adSquadId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/list-ads-by-ad-squad?${params}`, {
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
| `adSquadId` | string | yes | The Snapchat Ad Squad ID that owns the ads. |

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

Through the native Snapchat Ads API, this operation is `GET /adsquads/:adSquadId/ads` (base URL `https://adsapi.snapchat.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-ads-by-ad-squad.md) for the provider-specific parameters and requirements.

