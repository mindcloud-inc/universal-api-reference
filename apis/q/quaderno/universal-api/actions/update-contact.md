# Quaderno: Update Contact

Updates an existing contact in Quaderno.

```
PUT https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quaderno `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/update-contact', {
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
| `city` | string | no | Updated city. |
| `country` | string | no | Updated country. |
| `email` | string | no | Updated email address. |
| `firstName` | string | no | Updated first name. |
| `id` | string | yes | ID of the contact to update. |
| `notes` | string | no | Updated notes. |
| `postalCode` | string | no | Updated postal code. |
| `region` | string | no | Updated region. |
| `streetLine1` | string | no | Updated primary street address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "country": "string",
      "createdAt": 1,
      "email": "ava@example.com",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "id": 1,
      "kind": "string",
      "language": "string",
      "lastName": {},
      "notes": "string",
      "permalink": "https://example.com",
      "phone1": {},
      "postalCode": "string",
      "processor": {},
      "processorId": {},
      "region": "string",
      "streetLine1": "string",
      "streetLine2": {},
      "taxId": {},
      "taxStatus": "string",
      "web": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `country` | string |  |
| `createdAt` | number |  |
| `email` | string |  |
| `firstName` | string |  |
| `fullName` | string |  |
| `id` | number |  |
| `kind` | string |  |
| `language` | string |  |
| `lastName` | object |  |
| `notes` | string |  |
| `permalink` | string |  |
| `phone1` | object |  |
| `postalCode` | string |  |
| `processor` | object |  |
| `processorId` | object |  |
| `region` | string |  |
| `streetLine1` | string |  |
| `streetLine2` | object |  |
| `taxId` | object |  |
| `taxStatus` | string |  |
| `web` | object |  |

## Native endpoint

Through the native Quaderno API, this operation is `PUT /contacts/:id` (base URL `https://sandbox-quadernoapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

