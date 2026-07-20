# Freshworks CRM: Create Sales Activity

Creates a new sales activity in Freshworks CRM.

```
POST https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/create-sales-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/create-sales-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "salesActivity": {},
  "salesActivity.ownerId": 1,
  "salesActivity.salesActivityTypeId": 1,
  "salesActivity.targetableId": 1,
  "salesActivity.targetableType": "string",
  "salesActivity.title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/create-sales-activity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "salesActivity": {},
    "salesActivity.ownerId": 1,
    "salesActivity.salesActivityTypeId": 1,
    "salesActivity.targetableId": 1,
    "salesActivity.targetableType": "string",
    "salesActivity.title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `salesActivity` | object | yes |  |
| `salesActivity.endDate` | string | no |  |
| `salesActivity.notes` | string | no |  |
| `salesActivity.ownerId` | number | yes |  |
| `salesActivity.salesActivityOutcomeId` | number | no |  |
| `salesActivity.salesActivityTypeId` | number | yes |  |
| `salesActivity.startDate` | string | no |  |
| `salesActivity.targetableId` | number | yes |  |
| `salesActivity.targetableType` | string | yes |  |
| `salesActivity.title` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "sales_activity": {
        "conversation_time": "2026-05-07T12:00:00.000Z",
        "created_at": "2026-05-07T12:00:00.000Z",
        "creater_id": 1,
        "custom_field": {
          "cf_customer_option": true
        },
        "end_date": "2026-05-07T12:00:00.000Z",
        "id": 1,
        "latitude": "string",
        "location": "string",
        "longitude": "string",
        "notes": "string",
        "owner_id": 1,
        "sales_activity_outcome_id": 1,
        "sales_activity_type_id": 1,
        "start_date": "2026-05-07T12:00:00.000Z",
        "targetable_id": 1,
        "targetable_type": "string",
        "title": "string",
        "updated_at": "2026-05-07T12:00:00.000Z",
        "updater_id": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `sales_activity.conversation_time` | date |  |
| `sales_activity.created_at` | date |  |
| `sales_activity.creater_id` | number |  |
| `sales_activity.custom_field.cf_customer_option` | boolean |  |
| `sales_activity.end_date` | date |  |
| `sales_activity.id` | number |  |
| `sales_activity.latitude` | string |  |
| `sales_activity.location` | string |  |
| `sales_activity.longitude` | string |  |
| `sales_activity.notes` | string |  |
| `sales_activity.owner_id` | number |  |
| `sales_activity.sales_activity_outcome_id` | number |  |
| `sales_activity.sales_activity_type_id` | number |  |
| `sales_activity.start_date` | date |  |
| `sales_activity.targetable_id` | number |  |
| `sales_activity.targetable_type` | string |  |
| `sales_activity.title` | string |  |
| `sales_activity.updated_at` | date |  |
| `sales_activity.updater_id` | number |  |

## Native endpoint

Through the native Freshworks CRM API, this operation is `POST /api/sales_activities` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sales-activity.md) for the provider-specific parameters and requirements.

