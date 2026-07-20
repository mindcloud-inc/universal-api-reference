# Reddit Lead Ads: List Pixels By Business

Retrieves pixels for a business from Reddit Ads.

```
GET https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/list-pixels-by-business
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reddit Lead Ads `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/list-pixels-by-business?connectionId=$CONNECTION_ID&limit=25&offset=0&businessId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "businessId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/list-pixels-by-business?${params}`, {
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
| `businessId` | string | yes | The ID of the business to list pixels for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Pixel identifier. |
| `name` | string | Pixel name. |

## Native endpoint

Through the native Reddit Lead Ads API, this operation is `GET /businesses/{business_id}/pixels` (base URL `https://ads-api.reddit.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-pixels-by-business.md) for the provider-specific parameters and requirements.

