# Zenkit: Edit List Properties

Updates an existing list in Zenkit.

```
PUT https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/edit-list-properties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenkit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/edit-list-properties" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listAllId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/edit-list-properties', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listAllId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listAllId` | string | yes | The list all id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appType": "string",
      "backgroundId": "string",
      "coverImageId": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "created_by": 1,
      "defaultViewModus": 1,
      "deprecated_at": "string",
      "description": "string",
      "formulaTSortOrder": "string",
      "frozen_at": "string",
      "iconBackgroundColor": "string",
      "iconClassNames": "Ava Chen",
      "iconColor": "string",
      "id": 1,
      "imageId": "string",
      "isBuilding": true,
      "isMigrating": true,
      "isPublic": true,
      "itemName": "Ava Chen",
      "itemNamePlural": "Ava Chen",
      "name": "Ava Chen",
      "properties": "string",
      "resourceType": "string",
      "scheduled_for_deletion_at": "string",
      "settings": "string",
      "shortId": "string",
      "sortOrder": 1,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "uuid": "string",
      "visibility": 1,
      "workspaceId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appType` | string |  |
| `backgroundId` | string |  |
| `coverImageId` | string |  |
| `created_at` | date |  |
| `created_by` | number |  |
| `defaultViewModus` | number |  |
| `deprecated_at` | string |  |
| `description` | string |  |
| `formulaTSortOrder` | string |  |
| `frozen_at` | string |  |
| `iconBackgroundColor` | string |  |
| `iconClassNames` | string |  |
| `iconColor` | string |  |
| `id` | number |  |
| `imageId` | string |  |
| `isBuilding` | boolean |  |
| `isMigrating` | boolean |  |
| `isPublic` | boolean |  |
| `itemName` | string |  |
| `itemNamePlural` | string |  |
| `name` | string |  |
| `properties` | string |  |
| `resourceType` | string |  |
| `scheduled_for_deletion_at` | string |  |
| `settings` | string |  |
| `shortId` | string |  |
| `sortOrder` | number |  |
| `updated_at` | date |  |
| `uuid` | string |  |
| `visibility` | number |  |
| `workspaceId` | number |  |

## Native endpoint

Through the native Zenkit API, this operation is `PUT /lists/:listAllId` (base URL `https://zenkit.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-list-properties.md) for the provider-specific parameters and requirements.

