# SignWell: Get Template

Retrieves template details and fields from SignWell.

```
GET https://connect.mindcloud.co/v1/universal/signWell/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignWell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signWell/latest/actions/get-template?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signWell/latest/actions/get-template?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowDecline": {},
      "allowReassign": {},
      "apiApplicationId": {},
      "applySigningOrder": true,
      "archived": true,
      "createdAt": "string",
      "declineRedirectUrl": {},
      "embeddedEditUrl": "https://example.com",
      "expiresIn": {},
      "fields": [
        {}
      ],
      "files": [
        {
          "name": "Ava Chen",
          "pagesNumber": 1
        }
      ],
      "id": "string",
      "language": "string",
      "message": "string",
      "metadata": {},
      "name": "Ava Chen",
      "placeholders": [
        {
          "id": "string",
          "message": {},
          "name": "Ava Chen",
          "signingOrder": {},
          "subject": {}
        }
      ],
      "redirectUrl": {},
      "reminders": {},
      "requesterEmailAddress": "ava@example.com",
      "status": "string",
      "subject": "string",
      "templateLink": "https://example.com",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowDecline` | object |  |
| `allowReassign` | object |  |
| `apiApplicationId` | object |  |
| `applySigningOrder` | boolean |  |
| `archived` | boolean |  |
| `createdAt` | string |  |
| `declineRedirectUrl` | object |  |
| `embeddedEditUrl` | string |  |
| `expiresIn` | object |  |
| `fields[]` | object |  |
| `files[].name` | string |  |
| `files[].pagesNumber` | number |  |
| `id` | string |  |
| `language` | string |  |
| `message` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `placeholders[].id` | string |  |
| `placeholders[].message` | object |  |
| `placeholders[].name` | string |  |
| `placeholders[].signingOrder` | object |  |
| `placeholders[].subject` | object |  |
| `redirectUrl` | object |  |
| `reminders` | object |  |
| `requesterEmailAddress` | string |  |
| `status` | string |  |
| `subject` | string |  |
| `templateLink` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native SignWell API, this operation is `GET /document_templates/:id` (base URL `https://www.signwell.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.

