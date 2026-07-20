# Zenkit: Add Element To List

Creates a custom field in a Zenkit list.

```
POST https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/add-element-to-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenkit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/add-element-to-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": "string",
  "items": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/add-element-to-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": "string",
    "items": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listId` | string | yes | The list id |
| `items` | object | yes | JSON array of Zenkit field definitions. Zenkit runtime currently requires lowercase `elementcategory` in each object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "deprecated_at": "string",
      "description": "string",
      "displayName": "Ava Chen",
      "elementcategory": 1,
      "id": 1,
      "isAutoCreated": true,
      "isPrimary": true,
      "listId": 1,
      "name": "Ava Chen",
      "resourceRole": "string",
      "shortId": "string",
      "sortOrder": 1,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `deprecated_at` | string |  |
| `description` | string |  |
| `displayName` | string |  |
| `elementcategory` | number |  |
| `id` | number |  |
| `isAutoCreated` | boolean |  |
| `isPrimary` | boolean |  |
| `listId` | number |  |
| `name` | string |  |
| `resourceRole` | string |  |
| `shortId` | string |  |
| `sortOrder` | number |  |
| `updated_at` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native Zenkit API, this operation is `POST /lists/:listId/elements` (base URL `https://zenkit.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-element-to-list.md) for the provider-specific parameters and requirements.

