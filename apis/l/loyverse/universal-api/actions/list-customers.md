# Loyverse: List Customers

Retrieves customer records from the Loyverse database.

```
GET https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loyverse `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/list-customers?${params}`, {
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
| `customerIds` | string | no | Return only customers specified by a comma-separated list of IDs |
| `email` | string | no | Filter customers by email |
| `createdAtMin` | date | no | Show resources created after date (ISO 8601 format, e.g: 2020-03-30T18:30:00.000Z) |
| `createdAtMax` | date | no | Show resources created before date (ISO 8601 format, e.g: 2020-03-30T18:30:00.000Z) |
| `updatedAtMin` | string | no | Show resources updated after date (ISO 8601 format, e.g: 2020-03-30T18:30:00.000Z) |
| `updatedAtMax` | string | no | Show resources updated before date (ISO 8601 format, e.g: 2020-03-30T18:30:00.000Z) |
| `limit` | number | no | Used for pagination |
| `cursor` | string | no | Used for pagination |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customers": [
        {
          "address": "string",
          "city": "string",
          "countryCode": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "customerCode": "string",
          "deletedAt": "2026-05-07T12:00:00.000Z",
          "email": "ava@example.com",
          "firstVisit": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "lastVisit": "2026-05-07T12:00:00.000Z",
          "name": "Ava Chen",
          "note": "string",
          "permanentDeletionAt": "2026-05-07T12:00:00.000Z",
          "phoneNumber": "string",
          "postalCode": "string",
          "region": "string",
          "totalPoints": 1,
          "totalSpent": 1,
          "totalVisits": 1,
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customers` | array<object> |  |
| `customers[].address` | string | The customer's address |
| `customers[].city` | string | The customer's city, town, or village. |
| `customers[].countryCode` | string | The two-letter country code corresponding to the customer's country in ISO 3166-1-alpha-2 format. |
| `customers[].createdAt` | date | The time when this resource was created (ISO 8601 format, e.g. 2020-03-25T19:55:23.077Z) |
| `customers[].customerCode` | string |  |
| `customers[].deletedAt` | date | The time when this resource was deleted (ISO 8601 format, e.g. 2020-04-02T23:45:20.050Z) |
| `customers[].email` | string | The customer's email |
| `customers[].firstVisit` | date | The date of the first customer visit |
| `customers[].id` | string | The customer id. If included in the POST request it will cause an update instead of a creating a new object. |
| `customers[].lastVisit` | date | The date of the most recent customer visit |
| `customers[].name` | string | The customer's name |
| `customers[].note` | string | The note about the customer |
| `customers[].permanentDeletionAt` | date | The time when the customer data will be permanently deleted (usually 24 hours after soft deletion) |
| `customers[].phoneNumber` | string | The customer's phone number |
| `customers[].postalCode` | string | The customer’s postal code, also known as zip, postcode, Eircode, etc. |
| `customers[].region` | string | The customer’s region name. Typically a province, a state, or a prefecture. |
| `customers[].totalPoints` | number | Actual customer points balance |
| `customers[].totalSpent` | number | The total money amount that customer had spent |
| `customers[].totalVisits` | number | The total number of visits |
| `customers[].updatedAt` | date | The time when this resource was updated (ISO 8601 format, e.g. 2020-03-30T08:05:10.020Z) |

## Native endpoint

Through the native Loyverse API, this operation is `GET /customers` (base URL `https://api.loyverse.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

