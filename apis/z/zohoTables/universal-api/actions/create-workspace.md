# Zoho Tables: Create Workspace

Creates a new workspace in Zoho Tables.

```
POST https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/create-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Tables `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/create-workspace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "portalId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/create-workspace', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "portalId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `portalId` | number | yes |  |
| `workspaceName` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdBy": "string",
      "createdByMailId": "string",
      "createdTime": 1,
      "isHomeWorkspace": true,
      "lastModifiedBy": "string",
      "lastModifiedByMailId": "string",
      "lastModifiedTime": 1,
      "name": "Ava Chen",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdBy` | string | Workspace creator name. |
| `createdByMailId` | string | Workspace creator email. |
| `createdTime` | number | Workspace creation timestamp. |
| `isHomeWorkspace` | boolean | Whether this is the home workspace. |
| `lastModifiedBy` | string | Last modifier name. |
| `lastModifiedByMailId` | string | Last modifier email. |
| `lastModifiedTime` | number | Workspace last modified timestamp. |
| `name` | string | Workspace name. |
| `workspaceId` | string | Zoho workspace identifier. |

## Native endpoint

Through the native Zoho Tables API, this operation is `POST /workspaces` (base URL `https://tables.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-workspace.md) for the provider-specific parameters and requirements.

