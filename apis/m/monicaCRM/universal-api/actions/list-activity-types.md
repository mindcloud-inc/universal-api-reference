# Monica CRM: List Activity Types

Retrieves activity types from Monica CRM.

```
GET https://connect.mindcloud.co/v1/universal/monicaCRM/latest/actions/list-activity-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Monica CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monicaCRM/latest/actions/list-activity-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monicaCRM/latest/actions/list-activity-types?${params}`, {
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

Through the native Monica CRM API, this operation is `GET /activitytypes` (base URL `https://app.monicahq.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-activity-types.md) for the provider-specific parameters and requirements.

