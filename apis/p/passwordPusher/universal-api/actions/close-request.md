# Password Pusher: Close Request

Closes an existing request in Password Pusher.

```
DELETE https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/close-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Password Pusher `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/close-request?connectionId=$CONNECTION_ID&urlToken=orpw2wkg00vpn0a" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "urlToken": "orpw2wkg00vpn0a"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/close-request?${params}`, {
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
| `urlToken` | string | yes | The request URL token to close. Example: `orpw2wkg00vpn0a`. |

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

Through the native Password Pusher API, this operation is `DELETE /requests/{{urlToken}}` (base URL `https://eu.pwpush.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/close-request.md) for the provider-specific parameters and requirements.

