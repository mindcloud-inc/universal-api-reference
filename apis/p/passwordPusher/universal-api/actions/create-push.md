# Password Pusher: Create Push

Creates a secure push in Password Pusher.

```
POST https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/create-push
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Password Pusher `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/create-push" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "push.payload": "temporary onboarding password"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/create-push', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "push.payload": "temporary onboarding password"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `push.payload` | string | yes | The secret text to share. Example: `temporary onboarding password`. |
| `push.expireAfterDuration` | number | no | Duration enum from 0 to 17. Example: `6`. |
| `push.expireAfterViews` | number | no | Number of views before expiration, from 1 to 100. Example: `3`. |
| `push.kind` | string | no | Push type: text, file, url, or qr. JSON actions support text/url/qr payloads; file uploads require multipart form-data. Default: `text`. Example: `text`. |
| `push.name` | string | no | Optional dashboard name for the push. Example: `Database Credentials`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `push.passphrase` | string | no | Optional passphrase required to view the push. Example: `optional_passphrase`. |
| `push.note` | string | no | Internal note only visible to the creator. Example: `Internal note`. |
| `push.deletableByViewer` | boolean | no | Whether recipients may delete the push. |
| `push.retrievalStep` | boolean | no | Require an extra retrieval step. |
| `accountId` | number | no | Optional account ID for multi-account users. Example: `1`. |

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

Through the native Password Pusher API, this operation is `POST /pushes` (base URL `https://eu.pwpush.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-push.md) for the provider-specific parameters and requirements.

