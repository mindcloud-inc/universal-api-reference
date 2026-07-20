# WhautoChat: Update Contact by ID

Updates an existing contact in WhautoChat by ID.

```
PUT https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/update-contact-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhautoChat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/update-contact-by-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/update-contact-by-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | yes | Contact unique ID |
| `name` | string | no |  |
| `phoneNumber` | string | no |  |
| `workspace.id` | string | no |  |
| `stage` | string | no |  |
| `notes` | string | no |  |
| `customFields` | object | no |  |
| `tags[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customFields": {},
      "id": "string",
      "name": "Ava Chen",
      "notes": "string",
      "phoneNumber": "string",
      "stage": "string",
      "tags": [
        "string"
      ],
      "workspace": {
        "id": "string",
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customFields` | object |  |
| `id` | string |  |
| `name` | string |  |
| `notes` | string |  |
| `phoneNumber` | string |  |
| `stage` | string |  |
| `tags` | array<string> |  |
| `workspace.id` | string |  |
| `workspace.title` | string |  |

## Native endpoint

Through the native WhautoChat API, this operation is `PUT /v1/contacts/{contactId}` (base URL `https://api.whauto.chat`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact-by-id.md) for the provider-specific parameters and requirements.

