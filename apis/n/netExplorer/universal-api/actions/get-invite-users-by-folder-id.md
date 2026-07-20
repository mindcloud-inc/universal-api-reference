# NetExplorer: Get User



```
GET https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-invite-users-by-folder-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-invite-users-by-folder-id?connectionId=$CONNECTION_ID&folderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/get-invite-users-by-folder-id?${params}`, {
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
| `folderId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nbObjects": 1,
      "nbTotalObjects": 1,
      "objects": [
        {
          "emails": "ava@example.com",
          "id": 1,
          "name": "Ava Chen"
        }
      ],
      "offsetStart": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nbObjects` | number |  |
| `nbTotalObjects` | number |  |
| `objects` | array<object> |  |
| `objects[].emails` | string |  |
| `objects[].id` | number |  |
| `objects[].name` | string |  |
| `offsetStart` | number |  |

## Native endpoint

Through the native NetExplorer API, this operation is `GET /invite/users/:folderId` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invite-users-by-folder-id.md) for the provider-specific parameters and requirements.

