# Referral Factory: Search Users

Finds users in Referral Factory by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/referralFactory/latest/actions/search-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Referral Factory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/referralFactory/latest/actions/search-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/referralFactory/latest/actions/search-users?${params}`, {
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
      "campaign_id": 1,
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": 1,
      "qualified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign_id` | number | Campaign identifier for the user. |
| `email` | string | User email address. |
| `first_name` | string | User first name. |
| `id` | number | Referral Factory user identifier. |
| `qualified` | boolean | Whether the user is qualified. |

## Native endpoint

Through the native Referral Factory API, this operation is `POST /users/search` (base URL `https://referral-factory.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-users.md) for the provider-specific parameters and requirements.

