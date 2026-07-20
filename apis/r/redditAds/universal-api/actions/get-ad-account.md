# Reddit Lead Ads: Get Ad Account

Retrieves an ad account from Reddit Ads.

```
GET https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/get-ad-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reddit Lead Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/get-ad-account?connectionId=$CONNECTION_ID&adAccountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "adAccountId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/get-ad-account?${params}`, {
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
| `adAccountId` | string | yes | The ID of the ad account. |

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

Through the native Reddit Lead Ads API, this operation is `GET /ad_accounts/{ad_account_id}` (base URL `https://ads-api.reddit.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ad-account.md) for the provider-specific parameters and requirements.

