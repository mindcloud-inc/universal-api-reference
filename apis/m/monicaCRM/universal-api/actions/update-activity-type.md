# Monica CRM: Update Activity Type

Updates an existing activity type in Monica CRM.

```
PUT https://connect.mindcloud.co/v1/universal/monicaCRM/latest/actions/update-activity-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Monica CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/monicaCRM/latest/actions/update-activity-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "activityTypeCategoryId": "string",
  "activityTypeId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/monicaCRM/latest/actions/update-activity-type', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "activityTypeCategoryId": "string",
    "activityTypeId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `activityTypeCategoryId` | string | yes |  |
| `activityTypeId` | string | yes |  |
| `name` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "activity_type_category": {
          "id": 1,
          "name": "Ava Chen"
        },
        "created_at": "string",
        "id": 1,
        "location_type": "string",
        "name": "Ava Chen",
        "object": "string",
        "updated_at": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.activity_type_category.id` | number |  |
| `data.activity_type_category.name` | string |  |
| `data.created_at` | string |  |
| `data.id` | number |  |
| `data.location_type` | string |  |
| `data.name` | string |  |
| `data.object` | string |  |
| `data.updated_at` | string |  |

## Native endpoint

Through the native Monica CRM API, this operation is `PUT /activitytypes/:activityTypeId` (base URL `https://app.monicahq.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-activity-type.md) for the provider-specific parameters and requirements.

