# Wooxy: Send Email

Sends an email through your Wooxy account.

```
POST https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/send-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wooxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/send-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from.email": "no-reply@sender.example.com",
  "to.email": "apps@mindcloud.co",
  "subject": "Stage 3 Test Email",
  "html": "<html><body><p>Stage 3 test email</p></body></html>"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/send-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from.email": "no-reply@sender.example.com",
    "to.email": "apps@mindcloud.co",
    "subject": "Stage 3 Test Email",
    "html": "<html><body><p>Stage 3 test email</p></body></html>"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from.email` | string | yes | The sender email address on a verified Wooxy domain. Example: `no-reply@sender.example.com`. |
| `from.name` | string | no | Optional sender display name. Example: `MindCloud Test`. |
| `to.email` | string | yes | The recipient email address. Example: `apps@mindcloud.co`. |
| `to.name` | string | no | Optional recipient display name. Example: `Apps MindCloud`. |
| `subject` | string | yes | The message subject. Example: `Stage 3 Test Email`. |
| `html` | string | yes | The HTML body content. Example: `<html><body><p>Stage 3 test email</p></body></html>`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `text` | string | no | Optional plain-text body content. Example: `Stage 3 test email`. |

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

Through the native Wooxy API, this operation is `POST v3/mailer/send` (base URL `https://api.wooxy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-email.md) for the provider-specific parameters and requirements.

