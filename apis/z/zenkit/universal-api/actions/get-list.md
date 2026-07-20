# Zenkit: Get List

Retrieves a list from Zenkit.

```
GET https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/get-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenkit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/get-list?connectionId=$CONNECTION_ID&listShortId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listShortId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/get-list?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listShortId` | string | yes | The list ShortID. |

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

Through the native Zenkit API, this operation is `GET /lists/:listShortId` (base URL `https://zenkit.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list.md) for the provider-specific parameters and requirements.

