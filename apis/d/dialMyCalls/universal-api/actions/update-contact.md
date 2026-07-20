# DialMyCalls: Update Contact

Updates an existing contact in DialMyCalls.

```
PUT https://connect.mindcloud.co/v1/universal/dialMyCalls/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DialMyCalls `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dialMyCalls/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string",
  "phone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dialMyCalls/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string",
    "phone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | yes | The DialMyCalls contact ID to update. |
| `email` | string | no | The contact's email address. |
| `extension` | string | no | The contact's phone extension. |
| `extra1` | string | no | Miscellaneous data about this contact. |
| `firstname` | string | no | The contact's first name. |
| `groups[]` | array<string> | no | List of group IDs that this contact should belong to. |
| `lastname` | string | no | The contact's last name. |
| `phone` | string | yes | The contact's phone number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "col1": "string",
      "col2": "string",
      "col3": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "extra1": "string",
      "firstname": "Ava",
      "groups": [
        {}
      ],
      "id": "string",
      "lastname": "Chen",
      "phone": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `col1` | string |  |
| `col2` | string |  |
| `col3` | string |  |
| `createdAt` | date |  |
| `email` | string |  |
| `extra1` | string |  |
| `firstname` | string |  |
| `groups` | array<object> |  |
| `id` | string |  |
| `lastname` | string |  |
| `phone` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native DialMyCalls API, this operation is `PUT /contact/:ContactId` (base URL `https://{{credentials.apiKey}}@api.dialmycalls.com/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

