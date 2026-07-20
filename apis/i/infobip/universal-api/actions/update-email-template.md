# Infobip: Update Email Template



```
PUT https://connect.mindcloud.co/v1/universal/infobip/latest/actions/update-email-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infobip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/infobip/latest/actions/update-email-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": 1,
  "html": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/infobip/latest/actions/update-email-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": 1,
    "html": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | number | yes | Unique identifier (ID) of the email template. |
| `name` | string | no | Name of the email template. |
| `from` | string | no | Email address with optional sender name. |
| `replyTo` | string | no | Email address to which recipients of the email can reply. |
| `subject` | string | no | Subject of the email template. |
| `preheader` | string | no | Preheader of the email template. |
| `html` | string | yes | HTML content of the email template. |
| `attachments` | string | no | JSON string of attachments to be sent with the email template. |
| `landingPage` | string | no | The identifier of an opt out landing late to be used and displayed when an end user clicks the unsubscribe link. Create a landing page in your Infobip account and use the ID number. For example, 1_23456. If not present, the default opt out landing page is used. |

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

Through the native Infobip API, this operation is `PUT /email/1/templates/{templateId}` (base URL `https://rkpzwe.api.infobip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-email-template.md) for the provider-specific parameters and requirements.

