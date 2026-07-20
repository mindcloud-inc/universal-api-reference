# Ugosign: Update Contact

Updates an existing contact in Ugosign.

```
PUT https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ugosign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contact": "string",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contact": "string",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `city` | string | no |  |
| `contact` | string | yes |  |
| `country` | string | no |  |
| `email` | string | yes |  |
| `familyName` | string | no |  |
| `givenName` | string | no |  |
| `phoneNumber` | string | no |  |
| `website` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {
        "city": "string",
        "country": "string",
        "postalCode": "string",
        "street": "string",
        "street2": "string"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "familyName": "Ava Chen",
      "gender": "string",
      "givenName": "Ava Chen",
      "id": "string",
      "phoneNumber": "string",
      "position": "string",
      "privateComment": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.city` | string |  |
| `address.country` | string |  |
| `address.postalCode` | string |  |
| `address.street` | string |  |
| `address.street2` | string |  |
| `createdAt` | date |  |
| `email` | string |  |
| `familyName` | string |  |
| `gender` | string |  |
| `givenName` | string |  |
| `id` | string |  |
| `phoneNumber` | string |  |
| `position` | string |  |
| `privateComment` | string |  |
| `updatedAt` | date |  |
| `website` | string |  |

## Native endpoint

Through the native Ugosign API, this operation is `PATCH /v1/contacts/:contact` (base URL `https://app.ugosign.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

