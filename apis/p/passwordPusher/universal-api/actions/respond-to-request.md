# Password Pusher: Respond To Request

Responds to an open request in Password Pusher.

```
PUT https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/respond-to-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Password Pusher `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/respond-to-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "urlToken": "orpw2wkg00vpn0a",
  "request.response": "The requested credential is..."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/respond-to-request', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "urlToken": "orpw2wkg00vpn0a",
    "request.response": "The requested credential is..."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `urlToken` | string | yes | The request URL token to respond to. Example: `orpw2wkg00vpn0a`. |
| `request.response` | string | yes | The response text to submit to the request. Example: `The requested credential is...`. |

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
      "html_url": "https://example.com",
      "include_requestor": true,
      "json_url": "https://example.com",
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
| `close_after_at` | date |  |
| `close_after_duration` | number |  |
| `created_at` | date |  |
| `days_remaining` | number |  |
| `html_url` | string |  |
| `include_requestor` | boolean |  |
| `json_url` | string |  |
| `passphrase` | string |  |
| `response_file_attachments` | boolean |  |
| `retrieval_step` | boolean |  |
| `state` | string |  |
| `updated_at` | date |  |
| `url_token` | string |  |

## Native endpoint

Through the native Password Pusher API, this operation is `PATCH /requests/{{urlToken}}/respond` (base URL `https://eu.pwpush.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/respond-to-request.md) for the provider-specific parameters and requirements.

