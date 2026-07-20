# Dynamic Mockups: Create Collection

Creates a new collection in Dynamic Mockups.

```
POST https://connect.mindcloud.co/v1/universal/dynamicMockups/latest/actions/create-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dynamic Mockups `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dynamicMockups/latest/actions/create-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "e.g. Spring Collection"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dynamicMockups/latest/actions/create-collection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "e.g. Spring Collection"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the collection to create. Example: `e.g. Spring Collection`. |
| `catalog_uuid` | string | no | Optional catalog UUID to place this collection in. Example: `optional catalog UUID`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "catalogId": 1,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "id": 1,
        "isPublished": 1,
        "name": "Ava Chen",
        "slug": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "uuid": "string",
        "workspaceId": 1
      },
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.catalogId` | number |  |
| `data.createdAt` | date |  |
| `data.id` | number |  |
| `data.isPublished` | number |  |
| `data.name` | string |  |
| `data.slug` | string |  |
| `data.updatedAt` | date |  |
| `data.uuid` | string |  |
| `data.workspaceId` | number |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Dynamic Mockups API, this operation is `POST api/v1/collections` (base URL `https://app.dynamicmockups.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-collection.md) for the provider-specific parameters and requirements.

