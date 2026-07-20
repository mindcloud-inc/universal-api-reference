# Shuffll: List Assets

Retrieves assets from Shuffll.

```
GET https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/list-assets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shuffll `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/list-assets?connectionId=$CONNECTION_ID&organizationId=69cac8104c4a701fd26271a1&workspaceId=69cac8104c4a701fd26271a5" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "69cac8104c4a701fd26271a1",
  "workspaceId": "69cac8104c4a701fd26271a5"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/list-assets?${params}`, {
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
| `folder` | string | no | Optional folder filter. |
| `organizationId` | string | yes | Shuffll organization id. Default: `69cac8104c4a701fd26271a1`. |
| `type` | string | no | Optional asset type filter. |
| `workspaceId` | string | yes | Shuffll workspace id. Default: `69cac8104c4a701fd26271a5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "createdAt": "string",
      "displayName": "Ava Chen",
      "folder": "string",
      "mimetype": "string",
      "type": "string",
      "uploadPath": "string",
      "userEmail": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | Asset id. |
| `createdAt` | string | Creation timestamp. |
| `displayName` | string | Asset display name. |
| `folder` | string | Containing folder. |
| `mimetype` | string | Asset mime type. |
| `type` | string | Asset type. |
| `uploadPath` | string | Storage path. |
| `userEmail` | string | Owner email. |

## Native endpoint

Through the native Shuffll API, this operation is `GET /auth/organization/:organizationId/workspace/:workspaceId/assets` (base URL `https://api.shuffll.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-assets.md) for the provider-specific parameters and requirements.

