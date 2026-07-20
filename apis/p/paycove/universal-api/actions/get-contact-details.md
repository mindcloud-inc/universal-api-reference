# Paycove: Get Contact Details

Retrieves a contact from Paycove.

```
GET https://connect.mindcloud.co/v1/universal/paycove/latest/actions/get-contact-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paycove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paycove/latest/actions/get-contact-details?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paycove/latest/actions/get-contact-details?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Paycove CRMContact ID. Example: `1`. |

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

Through the native Paycove API, this operation is `GET contacts/:id` (base URL `https://paycove.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-details.md) for the provider-specific parameters and requirements.

