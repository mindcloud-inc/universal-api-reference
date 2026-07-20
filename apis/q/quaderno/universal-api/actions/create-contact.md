# Quaderno: Create Contact

Creates a new contact in Quaderno.

```
POST https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quaderno `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `city` | string | no | City for the contact. |
| `contactPerson` | string | no | Named contact person. |
| `country` | string | no | Two-letter country code for the contact. |
| `department` | string | no | Department name. |
| `firstName` | string | yes | Contact first name. |
| `fullName` | string | no | Full name for the contact. |
| `kind` | string | no | Whether the contact is a company or person. |
| `language` | string | no | Preferred language code. |
| `lastName` | string | no | Contact last name. |
| `notes` | string | no | Internal notes for the contact. |
| `phone1` | string | no | Primary phone number. |
| `postalCode` | string | no | Postal code for the contact. |
| `processor` | string | no | External processor name for the contact. |
| `processorId` | string | no | External processor identifier for the contact. |
| `region` | string | no | Region or state for the contact. |
| `streetLine1` | string | no | Primary street address. |
| `streetLine2` | string | no | Secondary street address. |
| `taxId` | string | no | Contact tax identification number. |
| `taxStatus` | string | no | Tax treatment for the contact. |
| `web` | string | no | Contact website URL. |
| `email` | string | no | Contact email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": {},
      "country": "string",
      "createdAt": 1,
      "email": "ava@example.com",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "id": 1,
      "kind": "string",
      "language": "string",
      "lastName": {},
      "notes": {},
      "permalink": "https://example.com",
      "phone1": {},
      "postalCode": {},
      "processor": {},
      "processorId": {},
      "region": {},
      "streetLine1": {},
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
| `city` | object |  |
| `country` | string |  |
| `createdAt` | number |  |
| `email` | string |  |
| `firstName` | string |  |
| `fullName` | string |  |
| `id` | number |  |
| `kind` | string |  |
| `language` | string |  |
| `lastName` | object |  |
| `notes` | object |  |
| `permalink` | string |  |
| `phone1` | object |  |
| `postalCode` | object |  |
| `processor` | object |  |
| `processorId` | object |  |
| `region` | object |  |
| `streetLine1` | object |  |
| `streetLine2` | object |  |
| `taxId` | object |  |
| `taxStatus` | string |  |
| `web` | object |  |

## Native endpoint

Through the native Quaderno API, this operation is `POST /contacts` (base URL `https://sandbox-quadernoapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

