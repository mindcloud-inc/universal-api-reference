# Password Pusher: Create Request

Creates a secure request in Password Pusher.

```
POST https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/create-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Password Pusher `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/create-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "request.request": "Please provide the API key here."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/create-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "request.request": "Please provide the API key here."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `request.request` | string | yes | The request text or message to share. Example: `Please provide the API key here.`. |
| `request.closeAfterDuration` | number | no | Duration enum from 0 to 17. Example: `8`. |
| `request.name` | string | no | Optional dashboard name for the request. Example: `Database Access Request`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `request.passphrase` | string | no | Optional passphrase required to view the request. Example: `optional_passphrase`. |
| `request.note` | string | no | Internal note only visible to the creator. Example: `Internal note`. |
| `request.retrievalStep` | boolean | no | Require an extra retrieval step. |
| `request.includeRequestor` | boolean | no | Include requestor information in the request. |
| `request.responseFileAttachments` | boolean | no | Allow responders to attach files. |
| `accountId` | number | no | Optional account ID for multi-account users. Example: `1`. |

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

Through the native Password Pusher API, this operation is `POST /requests` (base URL `https://eu.pwpush.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-request.md) for the provider-specific parameters and requirements.

