# Paycove: Update Contact

Updates a contact in Paycove.

```
PUT https://connect.mindcloud.co/v1/universal/paycove/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paycove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/paycove/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paycove/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Paycove CRMContact ID. Example: `1`. |
| `title` | string | no | Contact title. Example: `Manager`. |
| `name` | string | no | Full contact name. Example: `Jane Doe`. |
| `firstName` | string | no | Contact first name. Example: `Jane`. |
| `lastName` | string | no | Contact last name. Example: `Doe`. |
| `email` | string | no | Contact email. Example: `jane@example.com`. |
| `phone` | string | no | Contact phone. Example: `+1 555 0100`. |
| `mobile` | string | no | Contact mobile. Example: `+1 555 0101`. |
| `line1` | string | no | Street address. Example: `123 Main St`. |
| `city` | string | no | City. Example: `Austin`. |
| `state` | string | no | State or region. Example: `Texas`. |
| `country` | string | no | Country. Example: `US`. |
| `postalCode` | string | no | Postal code. Example: `78701`. |
| `ownerId` | string | no | Contact owner ID. Example: `11768907`. |
| `facebook` | string | no | Contact Facebook. Example: `https://facebook.com/example`. |
| `twitter` | string | no | Contact Twitter. Example: `https://x.com/example`. |
| `linkedin` | string | no | Contact LinkedIn. Example: `https://linkedin.com/in/example`. |
| `industry` | string | no | Contact industry. Example: `Software`. |
| `website` | string | no | Contact website. Example: `https://example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "city": {},
      "country": {},
      "createdAt": "string",
      "creatorId": {},
      "crmContactId": "string",
      "email": "ava@example.com",
      "facebook": {},
      "firstName": {},
      "id": 1,
      "industry": {},
      "invoiceTerms": 1,
      "lastName": {},
      "line1": {},
      "linkedin": {},
      "mobile": {},
      "name": "Ava Chen",
      "organizationId": {},
      "ownerId": {},
      "phone": {},
      "postalCode": {},
      "state": {},
      "title": {},
      "twitter": {},
      "updatedAt": "string",
      "website": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `city` | object |  |
| `country` | object |  |
| `createdAt` | string |  |
| `creatorId` | object |  |
| `crmContactId` | string |  |
| `email` | string |  |
| `facebook` | object |  |
| `firstName` | object |  |
| `id` | number |  |
| `industry` | object |  |
| `invoiceTerms` | number |  |
| `lastName` | object |  |
| `line1` | object |  |
| `linkedin` | object |  |
| `mobile` | object |  |
| `name` | string |  |
| `organizationId` | object |  |
| `ownerId` | object |  |
| `phone` | object |  |
| `postalCode` | object |  |
| `state` | object |  |
| `title` | object |  |
| `twitter` | object |  |
| `updatedAt` | string |  |
| `website` | object |  |

## Native endpoint

Through the native Paycove API, this operation is `PATCH contacts/:id` (base URL `https://paycove.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

