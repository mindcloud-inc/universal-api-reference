# RO App: List Orders



```
GET https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RO App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/list-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/list-orders?${params}`, {
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
| `types[]` | array<number> | no | List of Order Type IDs (same as order types) |
| `branches[]` | array<number> | no | List of Location IDs |
| `ids[]` | array<number> | no | List of Order IDs |
| `numbers[]` | array<number> | no | List of Order document numbers |
| `statuses[]` | array<number> | no | List of Order Status IDs |
| `managers[]` | array<number> | no | List of Employee IDs |
| `clientsIds[]` | array<number> | no | List of Client (Person / Organization) IDs |
| `clientNames[]` | array<string> | no | List of Client (Person / Organization) names |
| `clientPhones[]` | array<string> | no | List of phone numbers |
| `createdAt[]` | array<date> | no | Filter by creation date. Accepts an array with one or two ISO 8601 date-time values. If one value is provided, it represents the start (left) boundary. If two values are provided, they define a date range (start and end). Examples: ["2025-05-01T00:00:00Z"] — filter from May 1, 2025 onward. ["2025-05-01T00:00:00Z", "2025-05-02T00:00:00Z"] — filter between May 1 and May 2, 2025. |
| `modifiedAt[]` | array<date> | no | Filter by modification date. Accepts an array with one or two ISO 8601 date-time values. If one value is provided, it represents the start (left) boundary. If two values are provided, they define a date range (start and end). Examples: ["2025-05-01T00:00:00Z"] — filter from May 1, 2025 onward. ["2025-05-01T00:00:00Z", "2025-05-02T00:00:00Z"] — filter between May 1 and May 2, 2025. |
| `scheduledFor[]` | array<date> | no | Filter by "Scheduled from" date and time. Accepts an array with one or two ISO 8601 date-time values. If one value is provided, it represents the start (left) boundary. If two values are provided, they define a date range (start and end). Examples: ["2025-05-01T00:00:00Z"] — filter from May 1, 2025 onward. ["2025-05-01T00:00:00Z", "2025-05-02T00:00:00Z"] — filter between May 1 and May 2, 2025. |
| `dueDate[]` | array<date> | no | Filter by due date. Accepts an array with one or two ISO 8601 date-time values. If one value is provided, it represents the start (left) boundary. If two values are provided, they define a date range (start and end). Examples: ["2025-05-01T00:00:00Z"] — filter from May 1, 2025 onward. ["2025-05-01T00:00:00Z", "2025-05-02T00:00:00Z"] — filter between May 1 and May 2, 2025. |
| `assetUid[]` | array<string> | no | List of asset serial numbers (vin, imei) |
| `sort` | string | no | Defines the sorting order of returned results. Use a field name to sort ascending or prefix it with a minus sign (-) to sort descending. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ad_campaign_id": 1,
      "asset_id": 1,
      "assignee_id": 1,
      "branch_id": 1,
      "client_id": 1,
      "custom_fields": "string",
      "due_date": "2026-05-07T12:00:00.000Z",
      "engineer_notes": "string",
      "estimated_price": "string",
      "malfunction": "string",
      "manager_id": 1,
      "manager_notes": "string",
      "order_type_id": 1,
      "payer_id": 1,
      "resource_id": 1,
      "resume": "string",
      "scheduled_for": "2026-05-07T12:00:00.000Z",
      "scheduled_to": "2026-05-07T12:00:00.000Z",
      "urgent": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ad_campaign_id` | number |  |
| `asset_id` | number |  |
| `assignee_id` | number |  |
| `branch_id` | number |  |
| `client_id` | number |  |
| `custom_fields` | string |  |
| `due_date` | date |  |
| `engineer_notes` | string |  |
| `estimated_price` | string |  |
| `malfunction` | string |  |
| `manager_id` | number |  |
| `manager_notes` | string |  |
| `order_type_id` | number |  |
| `payer_id` | number |  |
| `resource_id` | number |  |
| `resume` | string |  |
| `scheduled_for` | date |  |
| `scheduled_to` | date |  |
| `urgent` | boolean |  |

## Native endpoint

Through the native RO App API, this operation is `GET /orders` (base URL `https://api.roapp.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

