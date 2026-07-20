# Freshworks CRM: Upsert Contact

Finds a contact in Freshworks CRM, or creates one if no match is found.

```
PUT https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/upsert-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/upsert-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contact": {},
  "uniqueIdentifier": {},
  "uniqueIdentifier.emails": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/upsert-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contact": {},
    "uniqueIdentifier": {},
    "uniqueIdentifier.emails": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contact` | object | yes |  |
| `contact.firstName` | string | no |  |
| `contact.lastName` | string | no |  |
| `uniqueIdentifier` | object | yes |  |
| `uniqueIdentifier.emails` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": {
        "display_name": "Ava Chen",
        "email": "ava@example.com",
        "first_name": "Ava",
        "id": 1,
        "last_name": "Chen",
        "mcr_id": 1,
        "type": "string",
        "updated_at": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact` | object |  |
| `contact.display_name` | string |  |
| `contact.email` | string |  |
| `contact.first_name` | string |  |
| `contact.id` | number |  |
| `contact.last_name` | string |  |
| `contact.mcr_id` | number |  |
| `contact.type` | string |  |
| `contact.updated_at` | date |  |

## Native endpoint

Through the native Freshworks CRM API, this operation is `POST /api/contacts/upsert` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-contact.md) for the provider-specific parameters and requirements.

