# Paycove: List Contacts

Retrieves contacts from Paycove.

```
GET https://connect.mindcloud.co/v1/universal/paycove/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paycove `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paycove/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paycove/latest/actions/list-contacts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "city": "string",
      "country": "string",
      "createdAt": "string",
      "creatorId": {},
      "crmContactId": "string",
      "email": "ava@example.com",
      "facebook": {},
      "firstName": "Ava",
      "id": 1,
      "industry": {},
      "invoiceTerms": 1,
      "lastName": "Chen",
      "line1": "string",
      "linkedin": {},
      "mobile": {},
      "name": "Ava Chen",
      "organizationId": {},
      "ownerId": {},
      "phone": "string",
      "postalCode": "string",
      "state": "string",
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
| `city` | string |  |
| `country` | string |  |
| `createdAt` | string |  |
| `creatorId` | object |  |
| `crmContactId` | string |  |
| `email` | string |  |
| `facebook` | object |  |
| `firstName` | string |  |
| `id` | number |  |
| `industry` | object |  |
| `invoiceTerms` | number |  |
| `lastName` | string |  |
| `line1` | string |  |
| `linkedin` | object |  |
| `mobile` | object |  |
| `name` | string |  |
| `organizationId` | object |  |
| `ownerId` | object |  |
| `phone` | string |  |
| `postalCode` | string |  |
| `state` | string |  |
| `title` | object |  |
| `twitter` | object |  |
| `updatedAt` | string |  |
| `website` | object |  |

## Native endpoint

Through the native Paycove API, this operation is `GET contacts` (base URL `https://paycove.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

