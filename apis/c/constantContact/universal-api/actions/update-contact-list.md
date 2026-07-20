# Constant Contact: Update Contact List

Updates a contact list in Constant Contact.

```
PUT https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/update-contact-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Constant Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/update-contact-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": "4f8fca3f-8f0c-4a07-bf8a-cfe8df3ed9a2",
  "name": "Prospects - Q2 2026"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/update-contact-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": "4f8fca3f-8f0c-4a07-bf8a-cfe8df3ed9a2",
    "name": "Prospects - Q2 2026"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listId` | string | yes | Unique ID of the contact list to update. Example: `4f8fca3f-8f0c-4a07-bf8a-cfe8df3ed9a2`. |
| `name` | string | yes | Updated contact list name. Example: `Prospects - Q2 2026`. |
| `favorite` | boolean | no | Whether to mark the list as favorite. Example: `true`. |
| `description` | string | no | Updated list description. Example: `Monthly product update recipients`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "favorite": true,
      "listId": "string",
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `deletedAt` | date |  |
| `description` | string |  |
| `favorite` | boolean |  |
| `listId` | string | Unique contact list ID. |
| `name` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Constant Contact API, this operation is `PUT /contact_lists/:list_id` (base URL `https://api.cc.email/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact-list.md) for the provider-specific parameters and requirements.

