# Password Pusher: List Open Requests

Retrieves open requests from Password Pusher.

```
GET https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/list-open-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Password Pusher `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/list-open-requests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/list-open-requests?${params}`, {
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
      "close_after_at": "2026-05-07T12:00:00.000Z",
      "close_after_duration": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "days_remaining": 1,
      "html_url": "https://example.com",
      "include_requestor": true,
      "json_url": "https://example.com",
      "name": "Ava Chen",
      "note": "string",
      "passphrase": "string",
      "response_file_attachments": true,
      "retrieval_step": true,
      "state": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url_token": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | number |  |
| `close_after_at` | date |  |
| `close_after_duration` | number |  |
| `created_at` | date |  |
| `days_remaining` | number |  |
| `html_url` | string |  |
| `include_requestor` | boolean |  |
| `json_url` | string |  |
| `name` | string |  |
| `note` | string |  |
| `passphrase` | string |  |
| `response_file_attachments` | boolean |  |
| `retrieval_step` | boolean |  |
| `state` | string |  |
| `updated_at` | date |  |
| `url_token` | string |  |

## Native endpoint

Through the native Password Pusher API, this operation is `GET /requests/open` (base URL `https://eu.pwpush.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-open-requests.md) for the provider-specific parameters and requirements.

