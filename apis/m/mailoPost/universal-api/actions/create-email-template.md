# MailoPost: Create Email Template

Creates a new email template in MailoPost.

```
POST https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/create-email-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailoPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/create-email-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fromEmail": "ava@example.com",
  "subject": "string",
  "html": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/create-email-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fromEmail": "ava@example.com",
    "subject": "string",
    "html": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fromEmail` | string | yes | Sender email address. |
| `subject` | string | yes | Template subject line. |
| `name` | string | no | Template name. |
| `text` | string | no | Plain-text template body. |
| `html` | string | yes | HTML template body. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fromName` | string | no | Sender display name. |
| `presetParams[]` | array<string> | no | Template substitution parameter names. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "from_email": "ava@example.com",
      "from_name": "Ava Chen",
      "html": true,
      "id": 1,
      "name": "Ava Chen",
      "preset_params": [
        "string"
      ],
      "state": "string",
      "subject": "string",
      "text": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `from_email` | string |  |
| `from_name` | string |  |
| `html` | boolean |  |
| `id` | number |  |
| `name` | string |  |
| `preset_params[]` | string |  |
| `state` | string |  |
| `subject` | string |  |
| `text` | boolean |  |

## Native endpoint

Through the native MailoPost API, this operation is `POST /email/templates` (base URL `https://api.mailopost.ru/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-email-template.md) for the provider-specific parameters and requirements.

