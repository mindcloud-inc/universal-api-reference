# Wooxy: Get Message Statistics

Retrieves email message statistics from Wooxy.

```
GET https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/get-message-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wooxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/get-message-statistics?connectionId=$CONNECTION_ID&ids%5B%5D=5d914c3dd132d5f45a4e3670" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids[]": "5d914c3dd132d5f45a4e3670"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/get-message-statistics?${params}`, {
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
| `ids[]` | array<string> | yes | An array of up to 100 Wooxy message IDs. Example: `5d914c3dd132d5f45a4e3670`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "emails": {
        "events": [
          {}
        ],
        "from": {},
        "headers": {},
        "html": "ava@example.com",
        "id": "ava@example.com",
        "status": "ava@example.com",
        "subject": "ava@example.com",
        "text": "ava@example.com",
        "to": {}
      },
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emails` | array<object> |  |
| `emails.events` | array<object> |  |
| `emails.from` | object |  |
| `emails.headers` | object |  |
| `emails.html` | string |  |
| `emails.id` | string |  |
| `emails.status` | string |  |
| `emails.subject` | string |  |
| `emails.text` | string |  |
| `emails.to` | object |  |
| `result` | boolean |  |

## Native endpoint

Through the native Wooxy API, this operation is `POST v3/mailer/info` (base URL `https://api.wooxy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message-statistics.md) for the provider-specific parameters and requirements.

