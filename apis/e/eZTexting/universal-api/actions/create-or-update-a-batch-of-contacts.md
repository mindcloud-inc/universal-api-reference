# EZ Texting: Create or Update a Batch of Contacts

Creates or updates multiple contacts in EZ Texting.

```
PUT https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/create-or-update-a-batch-of-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EZ Texting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/create-or-update-a-batch-of-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contacts[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/create-or-update-a-batch-of-contacts', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contacts[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contacts[]` | array<object> | yes | Contacts to create or update |
| `contacts[].phoneNumber` | string | no | Phone number Example: `(737) 337-8315`. |
| `contacts[].firstName` | string | no | First name |
| `contacts[].lastName` | string | no | Last name |
| `contacts[].email` | string | no | Email address |
| `contacts[].note` | string | no | Notes |
| `contacts[].custom1` | string | no | Custom value 1 |
| `contacts[].custom2` | string | no | Custom value 2 |
| `contacts[].custom3` | string | no | Custom value 3 |
| `contacts[].custom4` | string | no | Custom value 4 |
| `contacts[].custom5` | string | no | Custom value 5 |
| `contacts[].values` | object | no |  |
| `groupIdsAdd[]` | array<string> | no | Contact groups to add to each contact |
| `groupIdsRemove[]` | array<string> | no | Contact groups to remove from each contact |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EZ Texting API returns.

## Native endpoint

Through the native EZ Texting API, this operation is `POST /contacts/batch` (base URL `https://a.eztexting.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-a-batch-of-contacts.md) for the provider-specific parameters and requirements.

