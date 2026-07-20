# Starfish: Update Contact

Updates an existing contact in Starfish.

```
PUT https://connect.mindcloud.co/v1/universal/starfish/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starfish `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/starfish/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/starfish/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | number | yes | Contact ID. |
| `firstName` | string | no | Updated contact first name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "addressNumber": "string",
      "adminId": 1,
      "birthday": "2026-05-07T12:00:00.000Z",
      "chainId": 1,
      "city": "string",
      "company": "string",
      "contactId": 1,
      "contactUid": "string",
      "country": "string",
      "countryOrigin": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "gender": "string",
      "id": "string",
      "idIssueCountry": "string",
      "idNr": "string",
      "idType": "string",
      "invoices": [
        {}
      ],
      "lastModified": "2026-05-07T12:00:00.000Z",
      "lastName": "Chen",
      "location": [
        {}
      ],
      "meta": {},
      "name": "Ava Chen",
      "nationality": "string",
      "phone": "string",
      "phoneMobile": "string",
      "reservations": [
        {}
      ],
      "state": "string",
      "status": "string",
      "type": "string",
      "vatNumber": "string",
      "zipcode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `addressNumber` | string |  |
| `adminId` | number |  |
| `birthday` | date |  |
| `chainId` | number |  |
| `city` | string |  |
| `company` | string |  |
| `contactId` | number |  |
| `contactUid` | string |  |
| `country` | string |  |
| `countryOrigin` | string |  |
| `created` | date |  |
| `email` | string |  |
| `firstName` | string |  |
| `gender` | string |  |
| `id` | string |  |
| `idIssueCountry` | string |  |
| `idNr` | string |  |
| `idType` | string |  |
| `invoices` | array<object> |  |
| `lastModified` | date |  |
| `lastName` | string |  |
| `location` | array<object> |  |
| `meta` | object |  |
| `name` | string |  |
| `nationality` | string |  |
| `phone` | string |  |
| `phoneMobile` | string |  |
| `reservations` | array<object> |  |
| `state` | string |  |
| `status` | string |  |
| `type` | string |  |
| `vatNumber` | string |  |
| `zipcode` | string |  |

## Native endpoint

Through the native Starfish API, this operation is `PUT /contacts/:contact_id` (base URL `https://api.camping.care/v21`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

