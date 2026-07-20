# Seafile: Get Account Info

Retrieves the current account information from Seafile.

```
GET https://connect.mindcloud.co/v1/universal/seafile/latest/actions/get-account-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seafile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seafile/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seafile/latest/actions/get-account-info?${params}`, {
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
      "ai_cost": 1,
      "ai_credit": 1,
      "ai_usage_rate": "string",
      "avatar_url": "https://example.com",
      "collaborate_email_interval": 1,
      "contact_email": "ava@example.com",
      "department": "string",
      "email": "ava@example.com",
      "enable_subscription": true,
      "file_updates_email_interval": 1,
      "institution": "string",
      "is_org_staff": 1,
      "is_staff": true,
      "login_id": "string",
      "name": "Ava Chen",
      "space_usage": "string",
      "total": 1,
      "usage": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ai_cost` | number |  |
| `ai_credit` | number |  |
| `ai_usage_rate` | string |  |
| `avatar_url` | string |  |
| `collaborate_email_interval` | number |  |
| `contact_email` | string |  |
| `department` | string |  |
| `email` | string |  |
| `enable_subscription` | boolean |  |
| `file_updates_email_interval` | number |  |
| `institution` | string |  |
| `is_org_staff` | number |  |
| `is_staff` | boolean |  |
| `login_id` | string |  |
| `name` | string |  |
| `space_usage` | string |  |
| `total` | number |  |
| `usage` | number |  |

## Native endpoint

Through the native Seafile API, this operation is `GET https://plus.seafile.com/api2/account/info/` (base URL `https://plus.seafile.com/api2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-info.md) for the provider-specific parameters and requirements.

