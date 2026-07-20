# Sponsy: Update Customer

Updates a customer in Sponsy.

```
PUT https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sponsy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "string",
  "name": "Ava Chen",
  "contact.firstName": "Ava",
  "contact.lastName": "Chen",
  "contact.email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "string",
    "name": "Ava Chen",
    "contact.firstName": "Ava",
    "contact.lastName": "Chen",
    "contact.email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | list<string> | yes | Customer ID from List Customers. |
| `name` | string | yes | Customer name. |
| `contact` | object | no | Primary customer contact. |
| `contact.firstName` | string | yes | Primary contact first name. |
| `contact.lastName` | string | yes | Primary contact last name. |
| `contact.email` | string | yes | Primary contact email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowPortalReports": true,
      "archivedAt": "2026-05-07T12:00:00.000Z",
      "contacts": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "includeInMetrics": true,
      "name": "Ava Chen",
      "portalId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowPortalReports` | boolean | Whether portal reporting is enabled. |
| `archivedAt` | date | Archive timestamp when present. |
| `contacts` | array<object> | Primary and additional customer contacts. |
| `createdAt` | date | Customer creation timestamp. |
| `id` | string | Sponsy customer ID. |
| `includeInMetrics` | boolean | Whether the customer is included in metrics. |
| `name` | string | Customer name. |
| `portalId` | string | Customer portal ID. |
| `updatedAt` | date | Customer update timestamp. |
| `workspaceId` | string | Workspace ID for the customer. |

## Native endpoint

Through the native Sponsy API, this operation is `PATCH /v1/customers/:customerId` (base URL `https://api.getsponsy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

