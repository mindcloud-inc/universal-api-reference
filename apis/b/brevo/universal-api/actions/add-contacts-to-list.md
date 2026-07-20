# Brevo: Add Contacts to List



```
POST https://connect.mindcloud.co/v1/universal/brevo/latest/actions/add-contacts-to-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/add-contacts-to-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emails": {},
  "listId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/brevo/latest/actions/add-contacts-to-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emails": {},
    "listId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emails` | object<string> | yes | Array of contact emails to add to the list. Accepts multiple values as an array. |
| `ids` | list<number> | no | Array of contact IDs to add to the list. |
| `listId` | string | yes | Brevo list ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contacts": {
        "success": [
          "string"
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contacts.success[]` | string |  |

## Native endpoint

Through the native Brevo API, this operation is `POST /v3/contacts/lists/:listId/contacts/add` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-contacts-to-list.md) for the provider-specific parameters and requirements.

