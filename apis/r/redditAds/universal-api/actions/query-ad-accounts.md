# Reddit Lead Ads: Query Ad Accounts

Finds ad accounts for a business in Reddit Ads.

```
GET https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/query-ad-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reddit Lead Ads `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/query-ad-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0&businessId=string&data=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "businessId": "string",
  "data": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/query-ad-accounts?${params}`, {
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
| `businessId` | string | yes | The ID of the business to list ad accounts for. |
| `data` | object | yes | JSON request body from the Reddit Ads API spec. |

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
| `id` | string | Ad account identifier. |
| `name` | string | Ad account name. |

## Native endpoint

Through the native Reddit Lead Ads API, this operation is `POST /businesses/{business_id}/ad_accounts/query` (base URL `https://ads-api.reddit.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/query-ad-accounts.md) for the provider-specific parameters and requirements.

