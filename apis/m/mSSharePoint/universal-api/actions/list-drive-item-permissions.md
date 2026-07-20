# MS SharePoint: List Drive Item Permissions

Retrieves permissions for a SharePoint drive item.

```
GET https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/list-drive-item-permissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MS SharePoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/list-drive-item-permissions?connectionId=$CONNECTION_ID&driveId=string&itemId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "driveId": "string",
  "itemId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/list-drive-item-permissions?${params}`, {
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
| `driveId` | string | yes | Microsoft Graph drive ID. |
| `itemId` | string | yes | Drive item ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "grantedTo": {},
      "grantedToV2": {},
      "id": "string",
      "inheritedFrom": {},
      "link": {},
      "roles": [
        "string"
      ],
      "shareId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `grantedTo` | object |  |
| `grantedToV2` | object |  |
| `id` | string |  |
| `inheritedFrom` | object |  |
| `link` | object |  |
| `roles` | array<string> |  |
| `shareId` | string |  |

## Native endpoint

Through the native MS SharePoint API, this operation is `GET /v1.0/drives/{{driveId}}/items/{{itemId}}/permissions` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-drive-item-permissions.md) for the provider-specific parameters and requirements.

