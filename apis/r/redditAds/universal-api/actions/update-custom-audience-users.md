# Reddit Lead Ads: Update Custom Audience Users

Updates users in a custom audience in Reddit Ads.

```
PUT https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/update-custom-audience-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reddit Lead Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/update-custom-audience-users" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "audienceId": "string",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/update-custom-audience-users', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "audienceId": "string",
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `audienceId` | string | yes | Reddit Ads audience identifier. |
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
| `id` | string | Custom audience identifier. |
| `name` | string | Custom audience name. |
| `status` | string | Custom audience status. |

## Native endpoint

Through the native Reddit Lead Ads API, this operation is `PATCH /custom_audiences/{audience_id}/users` (base URL `https://ads-api.reddit.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-custom-audience-users.md) for the provider-specific parameters and requirements.

