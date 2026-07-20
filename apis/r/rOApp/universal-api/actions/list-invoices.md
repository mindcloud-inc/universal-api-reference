# RO App: List Invoices



```
GET https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RO App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/list-invoices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/list-invoices?${params}`, {
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
| `page` | number | no | Page number |
| `legalEntityId` | number | no | Legal entity ID |
| `ids[]` | array<number> | no | List of Invoice IDs |
| `numbers[]` | array<string> | no | List of Invoice document numbers |
| `paymentMethod` | string | no | Invoice payment method |
| `statuses[]` | array<number> | no | List of Invoice status IDs |
| `clientIds[]` | array<number> | no | List of Client (Person / Organization) IDs |
| `payerIds[]` | array<number> | no | List of Payer IDs |
| `managers[]` | array<number> | no | List of Manager IDs |
| `createdAt[]` | array<date> | no | Filter by creation date. Accepts an array with one or two ISO 8601 date-time values. If one value is provided, it represents the start (left) boundary. If two values are provided, they define a date range (start and end). Examples: ["2025-05-01T00:00:00Z"] — filter from May 1, 2025 onward. ["2025-05-01T00:00:00Z", "2025-05-02T00:00:00Z"] — filter between May 1 and May 2, 2025. |
| `modifiedAt[]` | array<date> | no | Filter by modification date. Accepts an array with one or two ISO 8601 date-time values. If one value is provided, it represents the start (left) boundary. If two values are provided, they define a date range (start and end). Examples: ["2025-05-01T00:00:00Z"] — filter from May 1, 2025 onward. ["2025-05-01T00:00:00Z", "2025-05-02T00:00:00Z"] — filter between May 1 and May 2, 2025. |
| `issueDate[]` | array<date> | no | Filter by date of issue. Accepts an array with one or two ISO 8601 date-time values. If one value is provided, it represents the start (left) boundary. If two values are provided, they define a date range (start and end). Examples: ["2025-05-01T00:00:00Z"] — filter from May 1, 2025 onward. ["2025-05-01T00:00:00Z", "2025-05-02T00:00:00Z"] — filter between May 1 and May 2, 2025. |
| `dueDate[]` | array<date> | no | Filter by due date. Accepts an array with one or two ISO 8601 date-time values. If one value is provided, it represents the start (left) boundary. If two values are provided, they define a date range (start and end). Examples: ["2025-05-01T00:00:00Z"] — filter from May 1, 2025 onward. ["2025-05-01T00:00:00Z", "2025-05-02T00:00:00Z"] — filter between May 1 and May 2, 2025. |
| `sort` | string | no | Defines the sorting order of returned results. Use a field name to sort ascending or prefix it with a minus sign (-) to sort descending. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "client": {
        "email": "ava@example.com",
        "id": 1,
        "name": "Ava Chen"
      },
      "createdAt": 1,
      "dueDate": 1,
      "id": 1,
      "idLabel": "string",
      "issueDate": 1,
      "managerId": 1,
      "payer": {
        "id": 1,
        "name": "Ava Chen"
      },
      "paymentType": 1,
      "products": [
        {
          "amount": 1,
          "id": 1,
          "price": 1,
          "title": "string"
        }
      ],
      "status": 1,
      "statusFull": {
        "color": "string",
        "id": 1,
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client` | object |  |
| `client.email` | string |  |
| `client.id` | number |  |
| `client.name` | string |  |
| `createdAt` | number |  |
| `dueDate` | number |  |
| `id` | number |  |
| `idLabel` | string |  |
| `issueDate` | number |  |
| `managerId` | number |  |
| `payer` | object |  |
| `payer.id` | number |  |
| `payer.name` | string |  |
| `paymentType` | number |  |
| `products` | array<object> |  |
| `products[].amount` | number |  |
| `products[].id` | number |  |
| `products[].price` | number |  |
| `products[].title` | string |  |
| `status` | number |  |
| `statusFull` | object |  |
| `statusFull.color` | string |  |
| `statusFull.id` | number |  |
| `statusFull.name` | string |  |

## Native endpoint

Through the native RO App API, this operation is `GET /invoices` (base URL `https://api.roapp.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

