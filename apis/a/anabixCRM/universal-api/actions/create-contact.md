# Anabix CRM: Create Contact

Creates a new contact in Anabix CRM.

```
POST https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anabix CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.email` | string | yes |  |
| `data.firstName` | string | no |  |
| `data.lastName` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customFields": [
        {}
      ],
      "description": "string",
      "email": "ava@example.com",
      "email2": "ava@example.com",
      "email3": "ava@example.com",
      "firstName": "Ava",
      "gdpr": {},
      "idContact": 1,
      "idOrganization": 1,
      "idOwner": 1,
      "lastName": "Chen",
      "lists": [
        {}
      ],
      "organization": "string",
      "phoneNumber": "string",
      "phoneNumber2": "string",
      "phoneNumber3": "string",
      "position": "string",
      "primaryContact": 1,
      "revisionInfo": {},
      "salutation": "string",
      "sex": "string",
      "shippingCity": "string",
      "shippingCode": "string",
      "shippingCountry": "string",
      "shippingStreet": "string",
      "source": "string",
      "title": "Ava Chen",
      "vip": 1,
      "website": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customFields` | array<object> |  |
| `description` | string |  |
| `email` | string |  |
| `email2` | string |  |
| `email3` | string |  |
| `firstName` | string |  |
| `gdpr` | object |  |
| `idContact` | number | Anabix contact ID. |
| `idOrganization` | number | Organization ID when present. |
| `idOwner` | number |  |
| `lastName` | string |  |
| `lists` | array<object> |  |
| `organization` | string |  |
| `phoneNumber` | string |  |
| `phoneNumber2` | string |  |
| `phoneNumber3` | string |  |
| `position` | string |  |
| `primaryContact` | number |  |
| `revisionInfo` | object |  |
| `salutation` | string |  |
| `sex` | string |  |
| `shippingCity` | string |  |
| `shippingCode` | string |  |
| `shippingCountry` | string |  |
| `shippingStreet` | string |  |
| `source` | string |  |
| `title` | string | Contact display title. |
| `vip` | number |  |
| `website` | string |  |

## Native endpoint

Through the native Anabix CRM API, this operation is `POST /api` (base URL `https://app.anabix.cz`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

