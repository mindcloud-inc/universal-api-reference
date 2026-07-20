# SignWell: Update Template

Updates an existing template in SignWell.

```
PUT https://connect.mindcloud.co/v1/universal/signWell/latest/actions/update-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignWell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/signWell/latest/actions/update-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signWell/latest/actions/update-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `name` | string | no | Updated template name. |
| `subject` | string | no | Updated email subject for the template. |
| `message` | string | no | Updated request message for the template. |

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

Through the native SignWell API, this operation is `PUT /document_templates/:id` (base URL `https://www.signwell.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-template.md) for the provider-specific parameters and requirements.

