# Halo Service Solutions: Create Sales Order

Creates a new sales order in Halo Service Solutions.

```
POST https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/create-sales-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Halo Service Solutions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/create-sales-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/create-sales-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `[]` | array<object> | no | Sales order payload array. |
| `[].title` | string | no | Sales order title. |
| `[].client_id` | number | no | Client ID for the sales order. |
| `[].user_id` | number | no | User ID for the sales order. |
| `[].site_id` | number | no | Site ID for the sales order. |
| `[].assigned_agent` | number | no | Assigned agent ID for the sales order. |
| `[].note` | string | no | Optional note for the sales order. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assigned_agent": 1,
      "client_id": 1,
      "client_name": "Ava Chen",
      "date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "note": "string",
      "open_status": 1,
      "quotation_id": 1,
      "site_id": 1,
      "site_name": "Ava Chen",
      "status": 1,
      "title": "string",
      "user_id": 1,
      "user_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assigned_agent` | number |  |
| `client_id` | number |  |
| `client_name` | string |  |
| `date` | date |  |
| `id` | number | Sales order ID |
| `note` | string |  |
| `open_status` | number |  |
| `quotation_id` | number |  |
| `site_id` | number |  |
| `site_name` | string |  |
| `status` | number |  |
| `title` | string |  |
| `user_id` | number |  |
| `user_name` | string |  |

## Native endpoint

Through the native Halo Service Solutions API, this operation is `POST /SalesOrder` (base URL `https://mindcloud.halopsa.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sales-order.md) for the provider-specific parameters and requirements.

