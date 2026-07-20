# Password Pusher: Retrieve Request

Retrieves a request response from Password Pusher.

```
GET https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/retrieve-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Password Pusher `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/retrieve-request?connectionId=$CONNECTION_ID&urlToken=orpw2wkg00vpn0a" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "urlToken": "orpw2wkg00vpn0a"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/retrieve-request?${params}`, {
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
| `urlToken` | string | yes | The request URL token from the secret URL. Example: `orpw2wkg00vpn0a`. |
| `passphrase` | string | no | Optional passphrase for passphrase-protected requests. Example: `optional_passphrase`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "close_after_at": "2026-05-07T12:00:00.000Z",
      "close_after_duration": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "days_remaining": 1,
      "files": [
        {
          "content_type": "string",
          "filename": "Ava Chen",
          "url": "https://example.com"
        }
      ],
      "html_url": "https://example.com",
      "include_requestor": true,
      "json_url": "https://example.com",
      "passphrase": "string",
      "request": "string",
      "response": "string",
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
| `close_after_at` | date |  |
| `close_after_duration` | number |  |
| `created_at` | date |  |
| `days_remaining` | number |  |
| `files` | array<object> |  |
| `files[].content_type` | string |  |
| `files[].filename` | string |  |
| `files[].url` | string |  |
| `html_url` | string |  |
| `include_requestor` | boolean |  |
| `json_url` | string |  |
| `passphrase` | string |  |
| `request` | string |  |
| `response` | string |  |
| `response_file_attachments` | boolean |  |
| `retrieval_step` | boolean |  |
| `state` | string |  |
| `updated_at` | date |  |
| `url_token` | string |  |

## Native endpoint

Through the native Password Pusher API, this operation is `GET /requests/{{urlToken}}` (base URL `https://eu.pwpush.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-request.md) for the provider-specific parameters and requirements.

