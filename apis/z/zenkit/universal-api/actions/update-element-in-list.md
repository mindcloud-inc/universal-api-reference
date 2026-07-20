# Zenkit: Update Element In List

Updates a custom field in a Zenkit list.

```
PUT https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/update-element-in-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenkit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/update-element-in-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "elementId": "string",
  "listId": "string",
  "item": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/update-element-in-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "elementId": "string",
    "listId": "string",
    "item": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `elementId` | string | yes | The element id |
| `listId` | string | yes | The list id |
| `item` | object | yes | JSON object for the Zenkit field update body. Zenkit runtime currently expects a single object, not an array. |

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

Through the native Zenkit API, this operation is `PUT /lists/:listId/elements/:elementId` (base URL `https://zenkit.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-element-in-list.md) for the provider-specific parameters and requirements.

