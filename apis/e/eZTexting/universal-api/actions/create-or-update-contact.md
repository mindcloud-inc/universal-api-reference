# EZ Texting: Create or Update Contact

Creates or updates a contact in EZ Texting.

```
PUT https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/create-or-update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EZ Texting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/create-or-update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/create-or-update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `custom1` | string | no | Custom value 1 |
| `custom2` | string | no | Custom value 2 |
| `custom3` | string | no | Custom value 3 |
| `custom4` | string | no | Custom value 4 |
| `custom5` | string | no | Custom value 5 |
| `email` | string | no | Contact email address |
| `firstName` | string | no | Contact first name |
| `groupIdsAdd[]` | array<string> | no | Contact groups to add |
| `groupIdsRemove[]` | array<string> | no | Contact groups to remove |
| `lastName` | string | no | Contact last name |
| `note` | string | no | Contact note |
| `phoneNumber` | string | no | Contact phone number Example: `(737) 337-8315`. |
| `values` | object | no | Additional dynamic contact values |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native EZ Texting API, this operation is `POST /contacts` (base URL `https://a.eztexting.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-contact.md) for the provider-specific parameters and requirements.

