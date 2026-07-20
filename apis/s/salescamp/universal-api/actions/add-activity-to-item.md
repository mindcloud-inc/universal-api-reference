# Salescamp: Add Activity to Item



```
POST https://connect.mindcloud.co/v1/universal/salescamp/latest/actions/add-activity-to-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salescamp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/salescamp/latest/actions/add-activity-to-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "string",
  "itemId": "string",
  "action": "string",
  "title": "string",
  "date": "string",
  "time": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salescamp/latest/actions/add-activity-to-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "string",
    "itemId": "string",
    "action": "string",
    "title": "string",
    "date": "string",
    "time": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collectionId` | string | yes | Resource ID of the collection |
| `itemId` | string | yes | Resource ID of the item |
| `action` | string | yes | Activity type such as meeting |
| `title` | string | yes | Activity title |
| `description` | string | no | Activity description |
| `date` | string | yes | Activity date |
| `time` | string | yes | Activity time |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": 1,
      "createdBy": "string",
      "createdOn": "string",
      "date": "string",
      "description": "string",
      "id": "string",
      "time": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | number |  |
| `createdBy` | string |  |
| `createdOn` | string |  |
| `date` | string |  |
| `description` | string |  |
| `id` | string |  |
| `time` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Salescamp API, this operation is `POST /v1/collections/:collectionId/items/:itemId/activities` (base URL `https://api.salescamp.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-activity-to-item.md) for the provider-specific parameters and requirements.

