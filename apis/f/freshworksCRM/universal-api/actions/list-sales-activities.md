# Freshworks CRM: List Sales Activities

Retrieves sales activities from Freshworks CRM.

```
GET https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/list-sales-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/list-sales-activities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/list-sales-activities?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {
        "total": 1,
        "total_pages": 1
      },
      "sales_activities": [
        {
          "checkedin_at": "2026-05-07T12:00:00.000Z",
          "conversation_time": "2026-05-07T12:00:00.000Z",
          "created_at": "2026-05-07T12:00:00.000Z",
          "creater_id": 1,
          "custom_field": {
            "cf_customer_option": true
          },
          "end_date": "2026-05-07T12:00:00.000Z",
          "id": 1,
          "import_id": 1,
          "latitude": "string",
          "location": "string",
          "longitude": "string",
          "notes": "string",
          "owner_id": 1,
          "remote_id": 1,
          "sales_activity_outcome_id": 1,
          "sales_activity_type_id": 1,
          "start_date": "2026-05-07T12:00:00.000Z",
          "targetable_id": 1,
          "targetable_type": "string",
          "title": "string",
          "updated_at": "2026-05-07T12:00:00.000Z",
          "updater_id": 1
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
| `meta.total` | number | Total count. |
| `meta.total_pages` | number | Total pages. |
| `sales_activities[].checkedin_at` | date | Check-in timestamp. |
| `sales_activities[].conversation_time` | date | Conversation timestamp. |
| `sales_activities[].created_at` | date | Created timestamp. |
| `sales_activities[].creater_id` | number | Creator user id. |
| `sales_activities[].custom_field.cf_customer_option` | boolean | Custom customer option flag. |
| `sales_activities[].end_date` | date | End date/time. |
| `sales_activities[].id` | number | Sales activity identifier. |
| `sales_activities[].import_id` | number | Import id. |
| `sales_activities[].latitude` | string | Latitude. |
| `sales_activities[].location` | string | Location text. |
| `sales_activities[].longitude` | string | Longitude. |
| `sales_activities[].notes` | string | Activity notes. |
| `sales_activities[].owner_id` | number | Owner user id. |
| `sales_activities[].remote_id` | number | Remote id. |
| `sales_activities[].sales_activity_outcome_id` | number | Outcome id. |
| `sales_activities[].sales_activity_type_id` | number | Sales activity type id. |
| `sales_activities[].start_date` | date | Start date/time. |
| `sales_activities[].targetable_id` | number | Target record id. |
| `sales_activities[].targetable_type` | string | Target record type. |
| `sales_activities[].title` | string | Activity title. |
| `sales_activities[].updated_at` | date | Updated timestamp. |
| `sales_activities[].updater_id` | number | Updater user id. |

## Native endpoint

Through the native Freshworks CRM API, this operation is `GET api/sales_activities` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sales-activities.md) for the provider-specific parameters and requirements.

