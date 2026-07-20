# Pumble: List User Groups

Retrieves user groups from a Pumble workspace.

```
GET https://connect.mindcloud.co/v1/universal/pumble/latest/actions/list-user-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pumble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pumble/latest/actions/list-user-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pumble/latest/actions/list-user-groups?${params}`, {
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
      "createdBy": "string",
      "description": "string",
      "disabled": true,
      "handle": "string",
      "id": "string",
      "name": "Ava Chen",
      "workspaceId": "string",
      "workspaceUserIds": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdBy` | string |  |
| `description` | string |  |
| `disabled` | boolean |  |
| `handle` | string |  |
| `id` | string |  |
| `name` | string |  |
| `workspaceId` | string |  |
| `workspaceUserIds` | array<string> |  |

## Native endpoint

Through the native Pumble API, this operation is `GET /listUserGroups` (base URL `https://pumble-api-keys.addons.marketplace.cake.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-groups.md) for the provider-specific parameters and requirements.

