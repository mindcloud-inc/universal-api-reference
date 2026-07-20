# Wooxy: Send Batch Email

Sends a batch email through Wooxy.

```
POST https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/send-batch-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wooxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/send-batch-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from.email": "no-reply@sender.example.com",
  "subject": "Stage 3 Batch Test",
  "html": "<html><body><p>Stage 3 batch test</p></body></html>",
  "recipients[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/send-batch-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from.email": "no-reply@sender.example.com",
    "subject": "Stage 3 Batch Test",
    "html": "<html><body><p>Stage 3 batch test</p></body></html>",
    "recipients[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from.email` | string | yes | The sender email address on a verified Wooxy domain. Example: `no-reply@sender.example.com`. |
| `subject` | string | yes | The message subject. Example: `Stage 3 Batch Test`. |
| `html` | string | yes | The HTML body content. Example: `<html><body><p>Stage 3 batch test</p></body></html>`. |
| `recipients[]` | array<object> | yes | The recipient array, for example [{"email":"user@example.com"}]. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        "string"
      ],
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<string> |  |
| `result` | boolean |  |

## Native endpoint

Through the native Wooxy API, this operation is `POST v3/mailer/batch-send` (base URL `https://api.wooxy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-batch-email.md) for the provider-specific parameters and requirements.

