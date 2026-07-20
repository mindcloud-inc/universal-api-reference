# Infobip: Get Email Template



```
GET https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get-email-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infobip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get-email-template?connectionId=$CONNECTION_ID&templateId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get-email-template?${params}`, {
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
| `templateId` | number | yes | Unique identifier (ID) of the email template. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": {
        "contentType": "string",
        "fileName": "Ava Chen",
        "id": "string",
        "size": 1,
        "url": "https://example.com"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "from": "string",
      "html": "string",
      "id": 1,
      "imagePreviewUrl": "https://example.com",
      "isHtmlEditable": true,
      "landingPageId": "string",
      "name": "Ava Chen",
      "preheader": "string",
      "replyTo": "string",
      "subject": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<object> |  |
| `attachments.contentType` | string |  |
| `attachments.fileName` | string |  |
| `attachments.id` | string |  |
| `attachments.size` | number |  |
| `attachments.url` | string |  |
| `createdAt` | date |  |
| `from` | string |  |
| `html` | string |  |
| `id` | number |  |
| `imagePreviewUrl` | string |  |
| `isHtmlEditable` | boolean |  |
| `landingPageId` | string |  |
| `name` | string |  |
| `preheader` | string |  |
| `replyTo` | string |  |
| `subject` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Infobip API, this operation is `GET /email/1/templates/{templateId}` (base URL `https://rkpzwe.api.infobip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-template.md) for the provider-specific parameters and requirements.

