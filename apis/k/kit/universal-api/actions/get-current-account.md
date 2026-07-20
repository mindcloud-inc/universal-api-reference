# Kit: Get Current Account

Retrieves current account details from Kit.

```
GET https://connect.mindcloud.co/v1/universal/kit/latest/actions/get-current-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kit/latest/actions/get-current-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kit/latest/actions/get-current-account?${params}`, {
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
      "account": {
        "created_at": "2026-05-07T12:00:00.000Z",
        "id": 1,
        "name": "Ava Chen",
        "plan_type": "string",
        "primary_email_address": "ava@example.com",
        "timezone": {
          "friendly_name": "Ava Chen",
          "name": "Ava Chen",
          "utc_offset": "string"
        }
      },
      "user": {
        "email": "ava@example.com",
        "id": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | object |  |
| `account.created_at` | date |  |
| `account.id` | number |  |
| `account.name` | string |  |
| `account.plan_type` | string |  |
| `account.primary_email_address` | string |  |
| `account.timezone` | object |  |
| `account.timezone.friendly_name` | string |  |
| `account.timezone.name` | string |  |
| `account.timezone.utc_offset` | string |  |
| `user` | object |  |
| `user.email` | string |  |
| `user.id` | number |  |

## Native endpoint

Through the native Kit API, this operation is `GET /account` (base URL `https://api.kit.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-account.md) for the provider-specific parameters and requirements.

