# Zoho Tables: List Workspaces

Retrieves all workspaces from Zoho Tables.

```
GET https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/list-workspaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Tables `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/list-workspaces?connectionId=$CONNECTION_ID&portalId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "portalId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/list-workspaces?${params}`, {
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
| `portalId` | number | yes | Portal ID |

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

Through the native Zoho Tables API, this operation is `GET /workspaces` (base URL `https://tables.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspaces.md) for the provider-specific parameters and requirements.

