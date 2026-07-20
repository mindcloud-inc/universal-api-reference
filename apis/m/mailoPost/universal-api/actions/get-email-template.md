# MailoPost: Get Email Template

Retrieves an email template from MailoPost.

```
GET https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/get-email-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailoPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/get-email-template?connectionId=$CONNECTION_ID&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/get-email-template?${params}`, {
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

Through the native MailoPost API, this operation is `GET /email/templates/:template_id` (base URL `https://api.mailopost.ru/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-template.md) for the provider-specific parameters and requirements.

