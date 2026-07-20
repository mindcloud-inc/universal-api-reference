# UseINBOX: Create Contact List

Creates a contact list in UseINBOX.

```
POST https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/create-contact-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UseINBOX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/create-contact-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listName": "Ava Chen",
  "groupId": "string",
  "legislation": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/create-contact-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listName": "Ava Chen",
    "groupId": "string",
    "legislation": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listName` | string | yes | Contact list name. |
| `groupId` | string | yes | Group ID for the contact list. |
| `legislation` | number | yes | INBOX legislation value for the contact list. |

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

Through the native UseINBOX API, this operation is `POST /inbox/v1/contactlists` (base URL `https://useapi.useinbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact-list.md) for the provider-specific parameters and requirements.

