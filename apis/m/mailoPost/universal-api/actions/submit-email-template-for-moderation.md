# MailoPost: Submit Email Template For Moderation

Submits an email template for moderation in MailoPost.

```
PUT https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/submit-email-template-for-moderation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailoPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/submit-email-template-for-moderation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/submit-email-template-for-moderation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | MailoPost template identifier. |

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

Through the native MailoPost API, this operation is `PATCH /email/templates/:template_id/to_pending` (base URL `https://api.mailopost.ru/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-email-template-for-moderation.md) for the provider-specific parameters and requirements.

