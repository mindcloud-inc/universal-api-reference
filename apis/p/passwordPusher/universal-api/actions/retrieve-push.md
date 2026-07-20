# Password Pusher: Retrieve Push

Retrieves a push payload from Password Pusher.

```
GET https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/retrieve-push
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Password Pusher `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/retrieve-push?connectionId=$CONNECTION_ID&urlToken=fkwjfvhall92" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "urlToken": "fkwjfvhall92"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/retrieve-push?${params}`, {
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
| `urlToken` | string | yes | The push URL token from the secret URL. Example: `fkwjfvhall92`. |
| `passphrase` | string | no | Optional passphrase for passphrase-protected pushes. Example: `optional_passphrase`. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
      "files": [
        {
          "content_type": "string",
          "filename": "Ava Chen",
          "url": "https://example.com"
        }
      ],
      "html_url": "https://example.com",
      "json_url": "https://example.com",
      "passphrase": "string",
      "payload": "string",
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
| `files` | array<object> |  |
| `files[].content_type` | string |  |
| `files[].filename` | string |  |
| `files[].url` | string |  |
| `html_url` | string |  |
| `json_url` | string |  |
| `passphrase` | string |  |
| `payload` | string |  |
| `retrieval_step` | boolean |  |
| `updated_at` | date |  |
| `url_token` | string |  |
| `views_remaining` | number |  |

## Native endpoint

Through the native Password Pusher API, this operation is `GET /pushes/{{urlToken}}` (base URL `https://eu.pwpush.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-push.md) for the provider-specific parameters and requirements.

