# Zenkit: Get Workspaces And Lists

Retrieves workspaces and lists from Zenkit.

```
GET https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/get-workspaces-and-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenkit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/get-workspaces-and-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/get-workspaces-and-lists?${params}`, {
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
      "appType": "string",
      "backgroundId": "string",
      "coverImageId": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "created_by": 1,
      "deprecated_at": "string",
      "description": "string",
      "iconBackgroundColor": "string",
      "iconClassNames": "Ava Chen",
      "iconColor": "string",
      "id": 1,
      "imageId": "string",
      "isDefault": true,
      "lists": [
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
      "name": "Ava Chen",
      "organizationId": 1,
      "parentWorkspaceId": "string",
      "resourceType": "string",
      "shortId": "string",
      "sortOrder": "string",
      "transferOrganizationCount": 1,
      "transferOwnershipCount": 1,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "uuid": "string",
      "visibility": 1
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
| `deprecated_at` | string |  |
| `description` | string |  |
| `iconBackgroundColor` | string |  |
| `iconClassNames` | string |  |
| `iconColor` | string |  |
| `id` | number |  |
| `imageId` | string |  |
| `isDefault` | boolean |  |
| `lists[].appType` | string |  |
| `lists[].backgroundId` | string |  |
| `lists[].coverImageId` | string |  |
| `lists[].created_at` | date |  |
| `lists[].created_by` | number |  |
| `lists[].defaultViewModus` | number |  |
| `lists[].deprecated_at` | string |  |
| `lists[].description` | string |  |
| `lists[].formulaTSortOrder` | string |  |
| `lists[].frozen_at` | string |  |
| `lists[].iconBackgroundColor` | string |  |
| `lists[].iconClassNames` | string |  |
| `lists[].iconColor` | string |  |
| `lists[].id` | number |  |
| `lists[].imageId` | string |  |
| `lists[].isBuilding` | boolean |  |
| `lists[].isMigrating` | boolean |  |
| `lists[].isPublic` | boolean |  |
| `lists[].itemName` | string |  |
| `lists[].itemNamePlural` | string |  |
| `lists[].name` | string |  |
| `lists[].properties` | string |  |
| `lists[].resourceType` | string |  |
| `lists[].scheduled_for_deletion_at` | string |  |
| `lists[].settings` | string |  |
| `lists[].shortId` | string |  |
| `lists[].sortOrder` | number |  |
| `lists[].updated_at` | date |  |
| `lists[].uuid` | string |  |
| `lists[].visibility` | number |  |
| `lists[].workspaceId` | number |  |
| `name` | string |  |
| `organizationId` | number |  |
| `parentWorkspaceId` | string |  |
| `resourceType` | string |  |
| `shortId` | string |  |
| `sortOrder` | string |  |
| `transferOrganizationCount` | number |  |
| `transferOwnershipCount` | number |  |
| `updated_at` | date |  |
| `uuid` | string |  |
| `visibility` | number |  |

## Native endpoint

Through the native Zenkit API, this operation is `GET /users/me/workspacesWithLists` (base URL `https://zenkit.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspaces-and-lists.md) for the provider-specific parameters and requirements.

