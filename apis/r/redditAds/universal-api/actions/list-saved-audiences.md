# Reddit Lead Ads: List Saved Audiences

Retrieves saved audiences from Reddit Ads.

```
GET https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/list-saved-audiences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reddit Lead Ads `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/list-saved-audiences?connectionId=$CONNECTION_ID&limit=25&offset=0&adAccountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "adAccountId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/list-saved-audiences?${params}`, {
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
| `adAccountId` | string | yes | The ID of the ad account to list saved audiences for. |

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
| `id` | string | Saved audience identifier. |
| `name` | string | Saved audience name. |
| `status` | string | Saved audience status. |

## Native endpoint

Through the native Reddit Lead Ads API, this operation is `GET /ad_accounts/{ad_account_id}/saved_audiences` (base URL `https://ads-api.reddit.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-saved-audiences.md) for the provider-specific parameters and requirements.

