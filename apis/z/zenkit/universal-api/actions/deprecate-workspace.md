# Zenkit: Deprecate Workspace

Deprecates an existing workspace in Zenkit.

```
DELETE https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/deprecate-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenkit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/deprecate-workspace?connectionId=$CONNECTION_ID&workspaceAllId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceAllId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/deprecate-workspace?${params}`, {
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
      "deprecated_at": "2026-05-07T12:00:00.000Z",
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
| `deprecated_at` | date |  |
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

Through the native Zenkit API, this operation is `DELETE /workspaces/:workspaceAllId` (base URL `https://zenkit.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/deprecate-workspace.md) for the provider-specific parameters and requirements.

