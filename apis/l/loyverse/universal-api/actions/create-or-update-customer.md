# Loyverse: Create or Update Customer

Creates or updates a customer in Loyverse.

```
PUT https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/create-or-update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loyverse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/create-or-update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/create-or-update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no | The customer id. If included in the POST request it will cause an update instead of a creating a new object. |
| `name` | string | yes | The customer's name |
| `email` | string | no | The customer's email |
| `phoneNumber` | string | no | The customer's phone number |
| `address` | string | no | The customer's address |
| `city` | string | no | The customer's city, town, or village. |
| `region` | string | no | The customer’s region name. Typically a province, a state, or a prefecture. |
| `postalCode` | string | no | The customer’s postal code, also known as zip, postcode, Eircode, etc. |
| `countryCode` | string | no | The two-letter country code corresponding to the customer's country in ISO 3166-1-alpha-2 format. |
| `customerCode` | string | no |  |
| `note` | string | no | The note about the customer |
| `firstVisit` | date | no | The date of the first customer visit |
| `lastVisit` | date | no | The date of the most recent customer visit |
| `totalVisits` | number | no | The total number of visits |
| `totalSpent` | number | no | The total money amount that customer had spent |
| `totalPoints` | number | no | Actual customer points balance |
| `createdAt` | date | no | The time when this resource was created (ISO 8601 format, e.g. 2020-03-25T19:55:23.077Z) |
| `updatedAt` | date | no | The time when this resource was updated (ISO 8601 format, e.g. 2020-03-30T08:05:10.020Z) |
| `deletedAt` | date | no | The time when this resource was deleted (ISO 8601 format, e.g. 2020-04-02T23:45:20.050Z) |
| `permanentDeletionAt` | date | no | The time when the customer data will be permanently deleted (usually 24 hours after soft deletion) |

## Response

```json
{
  "success": true,
  "data": [
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | The customer's address |
| `city` | string | The customer's city, town, or village. |
| `countryCode` | string | The two-letter country code corresponding to the customer's country in ISO 3166-1-alpha-2 format. |
| `createdAt` | date | The time when this resource was created (ISO 8601 format, e.g. 2020-03-25T19:55:23.077Z) |
| `customerCode` | string |  |
| `deletedAt` | date | The time when this resource was deleted (ISO 8601 format, e.g. 2020-04-02T23:45:20.050Z) |
| `email` | string | The customer's email |
| `firstVisit` | date | The date of the first customer visit |
| `id` | string | The customer id. If included in the POST request it will cause an update instead of a creating a new object. |
| `lastVisit` | date | The date of the most recent customer visit |
| `name` | string | The customer's name |
| `note` | string | The note about the customer |
| `permanentDeletionAt` | date | The time when the customer data will be permanently deleted (usually 24 hours after soft deletion) |
| `phoneNumber` | string | The customer's phone number |
| `postalCode` | string | The customer’s postal code, also known as zip, postcode, Eircode, etc. |
| `region` | string | The customer’s region name. Typically a province, a state, or a prefecture. |
| `totalPoints` | number | Actual customer points balance |
| `totalSpent` | number | The total money amount that customer had spent |
| `totalVisits` | number | The total number of visits |
| `updatedAt` | date | The time when this resource was updated (ISO 8601 format, e.g. 2020-03-30T08:05:10.020Z) |

## Native endpoint

Through the native Loyverse API, this operation is `POST /customers` (base URL `https://api.loyverse.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-customer.md) for the provider-specific parameters and requirements.

