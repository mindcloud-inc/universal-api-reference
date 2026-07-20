# SmartRoutes: Update Customer



```
PUT https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartRoutes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | ID of the customer to update. |
| `name` | string | no | Name of the customer. |
| `account` | string | no | Account number of the customer. |
| `address` | string | no | Address of the customer. |
| `postcode` | string | no | Postcode for the customer address. |
| `lat` | number | no | Latitude of the customer location. |
| `lng` | number | no | Longitude of the customer location. |
| `phone` | string | no | Contact number of the customer. |
| `email` | string | no | Email of the customer. |
| `notes` | string | no | Notes for customer interaction. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": "string",
      "address": "string",
      "capacities": [
        {}
      ],
      "created": "2026-05-07T12:00:00.000Z",
      "customFields": [
        {}
      ],
      "id": 1,
      "lat": 1,
      "lng": 1,
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "notes": "string",
      "skills": [
        "string"
      ],
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | string | Customer account number. |
| `address` | string | Customer address. |
| `capacities` | array<object> | Customer capacities. |
| `created` | date | Customer creation timestamp. |
| `customFields` | array<object> | Customer custom fields. |
| `id` | number | SmartRoutes customer identifier. |
| `lat` | number | Customer latitude. |
| `lng` | number | Customer longitude. |
| `modified` | date | Customer last modified timestamp. |
| `name` | string | Customer display name. |
| `notes` | string | Customer notes. |
| `skills` | array<string> | Customer skills. |
| `tags` | array<string> | Customer tags. |

## Native endpoint

Through the native SmartRoutes API, this operation is `PUT /customers/:id` (base URL `https://api.smartroutes.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

