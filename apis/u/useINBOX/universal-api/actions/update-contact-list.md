# UseINBOX: Update Contact List

Updates an existing contact list in UseINBOX.

```
PUT https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/update-contact-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UseINBOX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/update-contact-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/update-contact-list', {
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
| `id` | string | yes | Contact list ID from INBOX. |
| `listName` | string | no | Updated contact list name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "groupId": "string",
      "id": "string",
      "legislation": 1,
      "listName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `groupId` | string |  |
| `id` | string |  |
| `legislation` | number |  |
| `listName` | string |  |

## Native endpoint

Through the native UseINBOX API, this operation is `PATCH /inbox/v1/contactlists/:id` (base URL `https://useapi.useinbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact-list.md) for the provider-specific parameters and requirements.

