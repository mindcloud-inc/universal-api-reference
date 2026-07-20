# Password Pusher: List Expired Pushes

Retrieves expired pushes from Password Pusher.

```
GET https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/list-expired-pushes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Password Pusher `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/list-expired-pushes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/list-expired-pushes?${params}`, {
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
      "account_id": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "days_remaining": 1,
      "deletable_by_viewer": true,
      "deleted": true,
      "expire_after_days": 1,
      "expire_after_duration": 1,
      "expire_after_views": 1,
      "expired": true,
      "expired_on": "2026-05-07T12:00:00.000Z",
      "expires_at": "2026-05-07T12:00:00.000Z",
      "expires_in": 1,
      "html_url": "https://example.com",
      "json_url": "https://example.com",
      "name": "Ava Chen",
      "note": "string",
      "passphrase": "string",
      "retrieval_step": true,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url_token": "https://example.com",
      "views_remaining": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | number |  |
| `created_at` | date |  |
| `days_remaining` | number |  |
| `deletable_by_viewer` | boolean |  |
| `deleted` | boolean |  |
| `expire_after_days` | number |  |
| `expire_after_duration` | number |  |
| `expire_after_views` | number |  |
| `expired` | boolean |  |
| `expired_on` | date |  |
| `expires_at` | date |  |
| `expires_in` | number |  |
| `html_url` | string |  |
| `json_url` | string |  |
| `name` | string |  |
| `note` | string |  |
| `passphrase` | string |  |
| `retrieval_step` | boolean |  |
| `updated_at` | date |  |
| `url_token` | string |  |
| `views_remaining` | number |  |

## Native endpoint

Through the native Password Pusher API, this operation is `GET /pushes/expired` (base URL `https://eu.pwpush.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-expired-pushes.md) for the provider-specific parameters and requirements.

