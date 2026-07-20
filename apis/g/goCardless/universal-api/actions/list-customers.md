# GoCardless: List Customers

Finds customers in your GoCardless account.

```
GET https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCardless `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goCardless/latest/actions/list-customers?${params}`, {
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
| `actionRequired` | boolean | no |  |
| `createdAt` | object | no |  |
| `createdAt.gt` | date | no |  |
| `createdAt.gte` | date | no |  |
| `createdAt.lt` | date | no |  |
| `createdAt.lte` | date | no |  |
| `currency` | list | no | One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`. |
| `sortField` | list | no | One of: `0`, `1`, `2`. |
| `sortDirection` | list | no | One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customers": [
        {
          "addressLine1": {},
          "addressLine2": {},
          "addressLine3": {},
          "city": {},
          "companyName": {},
          "countryCode": "string",
          "createdAt": "string",
          "danishIdentityNumber": {},
          "email": "ava@example.com",
          "familyName": "Ava Chen",
          "givenName": "Ava Chen",
          "id": "string",
          "language": "string",
          "phoneNumber": {},
          "postalCode": {},
          "region": {},
          "swedishIdentityNumber": {}
        }
      ],
      "meta": {
        "cursors": {
          "after": {},
          "before": {}
        },
        "limit": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customers[].addressLine1` | object |  |
| `customers[].addressLine2` | object |  |
| `customers[].addressLine3` | object |  |
| `customers[].city` | object |  |
| `customers[].companyName` | object |  |
| `customers[].countryCode` | string |  |
| `customers[].createdAt` | string |  |
| `customers[].danishIdentityNumber` | object |  |
| `customers[].email` | string |  |
| `customers[].familyName` | string |  |
| `customers[].givenName` | string |  |
| `customers[].id` | string |  |
| `customers[].language` | string |  |
| `customers[].phoneNumber` | object |  |
| `customers[].postalCode` | object |  |
| `customers[].region` | object |  |
| `customers[].swedishIdentityNumber` | object |  |
| `meta.cursors.after` | object |  |
| `meta.cursors.before` | object |  |
| `meta.limit` | number |  |

## Native endpoint

Through the native GoCardless API, this operation is `GET /customers` (base URL `https://api-sandbox.gocardless.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

