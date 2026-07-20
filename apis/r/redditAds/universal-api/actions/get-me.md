# Reddit Lead Ads: Get Me

Retrieves the authenticated user from Reddit Ads.

```
GET https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/get-me
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reddit Lead Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/get-me?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/get-me?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "firstname": "Ava",
      "id": "string",
      "lastname": "Chen",
      "phone": "string",
      "redditUsername": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Email address of the member. |
| `firstname` | string | The first name of the member. |
| `id` | string | The unique identifier of the member. |
| `lastname` | string | The last name of the member. |
| `phone` | string | The phone number of the member. |
| `redditUsername` | string | The Reddit username of the member. |

## Native endpoint

Through the native Reddit Lead Ads API, this operation is `GET /me` (base URL `https://ads-api.reddit.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-me.md) for the provider-specific parameters and requirements.

