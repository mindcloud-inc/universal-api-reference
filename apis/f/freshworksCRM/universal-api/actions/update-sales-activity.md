# Freshworks CRM: Update Sales Activity

Updates an existing sales activity in Freshworks CRM.

```
PUT https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/update-sales-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/update-sales-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "salesActivity": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/update-sales-activity', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "salesActivity": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `salesActivity` | object | yes |  |
| `salesActivity.notes` | string | no |  |
| `salesActivity.ownerId` | number | no |  |
| `salesActivity.targetableId` | number | no |  |
| `salesActivity.targetableType` | string | no |  |
| `salesActivity.title` | string | no |  |

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

Through the native Freshworks CRM API, this operation is `PUT /api/sales_activities/:id` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sales-activity.md) for the provider-specific parameters and requirements.

