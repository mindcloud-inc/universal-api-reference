# TranslatePlus: Translate Email

Translates email subject and HTML body in TranslatePlus.

```
POST https://connect.mindcloud.co/v1/universal/translatePlus/latest/actions/translate-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TranslatePlus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/translatePlus/latest/actions/translate-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subject": "string",
  "emailBody": "ava@example.com",
  "source": "string",
  "target": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/translatePlus/latest/actions/translate-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subject": "string",
    "emailBody": "ava@example.com",
    "source": "string",
    "target": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subject` | string | yes |  |
| `emailBody` | string | yes |  |
| `source` | string | yes |  |
| `target` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "html_body": "string",
      "subject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `html_body` | string |  |
| `subject` | string |  |

## Native endpoint

Through the native TranslatePlus API, this operation is `POST /v2/translate/email` (base URL `https://api.translateplus.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/translate-email.md) for the provider-specific parameters and requirements.

