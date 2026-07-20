# MailerSend: Get Template



```
GET https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/get-template?connectionId=$CONNECTION_ID&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/get-template?${params}`, {
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
| `templateId` | string | yes | ID of the MailerSend template. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": {},
      "createdAt": "string",
      "domain": {},
      "id": "string",
      "imagePath": "string",
      "name": "Ava Chen",
      "personalization": {},
      "templateStats": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | object | Template category metadata. |
| `createdAt` | string | Template creation timestamp. |
| `domain` | object | Domain metadata linked to the template. |
| `id` | string | MailerSend template ID. |
| `imagePath` | string | Preview image URL for the template. |
| `name` | string | Template display name. |
| `personalization` | object | Template personalization defaults. |
| `templateStats` | object | Usage statistics for the template. |
| `type` | string | Template type. |

## Native endpoint

Through the native MailerSend API, this operation is `GET /templates/:template_id` (base URL `https://api.mailersend.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.

