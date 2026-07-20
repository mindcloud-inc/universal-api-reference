# Brevo: Get SMTP Template



```
GET https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-smtp-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-smtp-template?connectionId=$CONNECTION_ID&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-smtp-template?${params}`, {
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
| `templateId` | string | yes | SMTP template ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "doiTemplate": true,
      "htmlContent": "string",
      "id": 1,
      "isActive": true,
      "modifiedAt": "string",
      "name": "Ava Chen",
      "replyTo": "string",
      "sender": {
        "email": "ava@example.com",
        "id": 1,
        "name": "Ava Chen"
      },
      "subject": "string",
      "tag": "string",
      "testSent": true,
      "toField": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `doiTemplate` | boolean |  |
| `htmlContent` | string |  |
| `id` | number |  |
| `isActive` | boolean |  |
| `modifiedAt` | string |  |
| `name` | string |  |
| `replyTo` | string |  |
| `sender.email` | string |  |
| `sender.id` | number |  |
| `sender.name` | string |  |
| `subject` | string |  |
| `tag` | string |  |
| `testSent` | boolean |  |
| `toField` | string |  |

## Native endpoint

Through the native Brevo API, this operation is `GET /v3/smtp/templates/:templateId` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-smtp-template.md) for the provider-specific parameters and requirements.

