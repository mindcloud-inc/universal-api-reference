# RO App: Create Estimate



```
POST https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/create-estimate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RO App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/create-estimate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "branchId": 1,
  "orderTypeId": 1,
  "clientId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/create-estimate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "branchId": 1,
    "orderTypeId": 1,
    "clientId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `branchId` | number | yes | Location ID |
| `orderTypeId` | number | yes | Estimate/Order Type ID |
| `managerId` | number | no | Manager ID |
| `assigneeId` | number | no | Assigned Employee ID |
| `assetId` | number | no | Asset ID |
| `clientId` | number | yes | Client (Person / Organization) ID |
| `payerId` | number | no | Payer (Person / Organization) ID |
| `adCampaignId` | number | no | Ad Campaign ID |
| `scheduledFor` | date | no | "Scheduled From" date and time (ISO 8601) |
| `scheduledTo` | date | no | "Scheduled To" date and time (ISO 8601) |
| `resourceId` | number | no | Resource ID |
| `malfunction` | string | no | Malfunction text |
| `managerNotes` | string | no | Manager notes |
| `engineerNotes` | string | no | Technician notes |
| `resume` | string | no | Conclusion / client recommendations |
| `estimatedPrice` | string | no | Estimates price or price range |
| `dueDate` | date | no | Estimate Due Date (ISO 8601) |
| `urgent` | boolean | no | Is Estimate urgent? |
| `customFields` | string | no | Custom fields values in format {"f123": "value", "f234": "value"}, where "f123" and "f234" is a custom field id. |

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

Through the native RO App API, this operation is `POST /estimates` (base URL `https://api.roapp.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-estimate.md) for the provider-specific parameters and requirements.

