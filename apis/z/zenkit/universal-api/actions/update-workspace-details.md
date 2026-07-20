# Zenkit: Update Workspace Details

Updates an existing workspace in Zenkit.

```
PUT https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/update-workspace-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenkit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/update-workspace-details" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceAllId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/update-workspace-details', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceAllId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceAllId` | string | yes | The workspace all id. |

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

Through the native Zenkit API, this operation is `PUT /workspaces/:workspaceAllId` (base URL `https://zenkit.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-workspace-details.md) for the provider-specific parameters and requirements.

