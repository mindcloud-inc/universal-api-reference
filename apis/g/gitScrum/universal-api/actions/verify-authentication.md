# GitScrum: Verify Authentication

Retrieves the authenticated GitScrum account details.

```
GET https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/verify-authentication
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitScrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/verify-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/verify-authentication?${params}`, {
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
      "avatar": "string",
      "country_id": 1,
      "created_at": {},
      "email_offers": true,
      "email_product_updates": true,
      "email_weekly": true,
      "headline": "string",
      "id": 1,
      "language": "string",
      "location": "string",
      "name": "Ava Chen",
      "onboarding_completed": true,
      "onboarding_started": true,
      "presence_status": "string",
      "theme": "string",
      "timezone_id": 1,
      "timezone_name": "Ava Chen",
      "username": "Ava Chen",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | string |  |
| `country_id` | number |  |
| `created_at` | object |  |
| `email_offers` | boolean |  |
| `email_product_updates` | boolean |  |
| `email_weekly` | boolean |  |
| `headline` | string |  |
| `id` | number |  |
| `language` | string |  |
| `location` | string |  |
| `name` | string |  |
| `onboarding_completed` | boolean |  |
| `onboarding_started` | boolean |  |
| `presence_status` | string |  |
| `theme` | string |  |
| `timezone_id` | number |  |
| `timezone_name` | string |  |
| `username` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native GitScrum API, this operation is `POST /auth/me` (base URL `https://services.gitscrum.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-authentication.md) for the provider-specific parameters and requirements.

