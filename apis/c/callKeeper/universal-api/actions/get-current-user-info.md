# CallKeeper: Get Current User Info

Retrieves current user information from CallKeeper.

```
GET https://connect.mindcloud.co/v1/universal/callKeeper/latest/actions/get-current-user-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallKeeper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callKeeper/latest/actions/get-current-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callKeeper/latest/actions/get-current-user-info?${params}`, {
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
      "avatar_url": "https://example.com",
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "email_verified": true,
      "first_name": "Ava",
      "id": "string",
      "is_active": true,
      "last_login_at": "2026-05-07T12:00:00.000Z",
      "last_name": "Chen",
      "phone": "string",
      "subscription_plan": "string",
      "subscription_status": "string",
      "timezone": "string",
      "twilio_phone_number": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar_url` | string | Avatar URL. |
| `created_at` | date | Creation timestamp. |
| `email` | string | User email address. |
| `email_verified` | boolean | Whether the user email is verified. |
| `first_name` | string | User first name. |
| `id` | string | CallKeeper user ID. |
| `is_active` | boolean | Whether the user is active. |
| `last_login_at` | date | Last login timestamp. |
| `last_name` | string | User last name. |
| `phone` | string | User phone number. |
| `subscription_plan` | string | Subscription plan. |
| `subscription_status` | string | Subscription status. |
| `timezone` | string | User timezone. |
| `twilio_phone_number` | string | Provisioned Twilio phone number. |

## Native endpoint

Through the native CallKeeper API, this operation is `GET /auth/me` (base URL `https://api.callkeeper.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user-info.md) for the provider-specific parameters and requirements.

