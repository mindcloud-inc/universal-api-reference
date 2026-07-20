# Bento Now: Create Sequence Email

Creates an email template in a Bento Now sequence.

```
POST https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/create-sequence-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bento Now `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/create-sequence-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email_template.html": "ava@example.com",
  "email_template.subject": "ava@example.com",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/create-sequence-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email_template.html": "ava@example.com",
    "email_template.subject": "ava@example.com",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email_template.html` | string | yes |  |
| `email_template.subject` | string | yes |  |
| `id` | string | yes |  |
| `email_template.delay_interval` | string | no | Optional delay unit: minutes, hours, days, or months. |
| `email_template.delay_interval_count` | number | no | Optional delay amount used with Delay Interval. |
| `email_template.editor_choice` | string | no | Optional editor mode. |
| `email_template.inbox_snippet` | string | no | Optional preview text snippet. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "html": "string",
        "name": "Ava Chen",
        "stats": {},
        "subject": "string"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.createdAt` | date |  |
| `attributes.html` | string |  |
| `attributes.name` | string |  |
| `attributes.stats` | object |  |
| `attributes.subject` | string |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Bento Now API, this operation is `POST /v1/fetch/sequences/:id/emails/templates` (base URL `https://app.bentonow.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sequence-email.md) for the provider-specific parameters and requirements.

