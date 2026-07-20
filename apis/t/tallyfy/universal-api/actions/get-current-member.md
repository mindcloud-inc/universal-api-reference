# Tallyfy: Get Current Member

Retrieves the current member from Tallyfy.

```
GET https://connect.mindcloud.co/v1/universal/tallyfy/latest/actions/get-current-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tallyfy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tallyfy/latest/actions/get-current-member?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tallyfy/latest/actions/get-current-member?${params}`, {
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
      "activated_at": "2026-05-07T12:00:00.000Z",
      "approved_at": "2026-05-07T12:00:00.000Z",
      "cadence_days": [
        "string"
      ],
      "country_id": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "date_format": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "full_name": "Ava Chen",
      "id": 1,
      "initial_signup_method": "string",
      "is_active": true,
      "is_default_admin": true,
      "is_partner": true,
      "is_support": true,
      "last_accessed_at": "2026-05-07T12:00:00.000Z",
      "last_city": "string",
      "last_country": "string",
      "last_known_country": "string",
      "last_known_ip": "string",
      "last_login_at": "2026-05-07T12:00:00.000Z",
      "last_name": "Chen",
      "phone": "string",
      "profile_pic": "string",
      "resize_profile_pic": "string",
      "role": "string",
      "status": "string",
      "step_preferences": true,
      "timezone": "string",
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "username": "Ava Chen",
      "UTC_offset": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activated_at` | date |  |
| `approved_at` | date |  |
| `cadence_days[]` | string |  |
| `country_id` | number |  |
| `created_at` | date |  |
| `date_format` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `full_name` | string |  |
| `id` | number |  |
| `initial_signup_method` | string |  |
| `is_active` | boolean |  |
| `is_default_admin` | boolean |  |
| `is_partner` | boolean |  |
| `is_support` | boolean |  |
| `last_accessed_at` | date |  |
| `last_city` | string |  |
| `last_country` | string |  |
| `last_known_country` | string |  |
| `last_known_ip` | string |  |
| `last_login_at` | date |  |
| `last_name` | string |  |
| `phone` | string |  |
| `profile_pic` | string |  |
| `resize_profile_pic` | string |  |
| `role` | string |  |
| `status` | string |  |
| `step_preferences` | boolean |  |
| `timezone` | string |  |
| `type` | string |  |
| `updated_at` | date |  |
| `username` | string |  |
| `UTC_offset` | string |  |

## Native endpoint

Through the native Tallyfy API, this operation is `GET /organizations/:org/me` (base URL `https://api.tallyfy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-member.md) for the provider-specific parameters and requirements.

