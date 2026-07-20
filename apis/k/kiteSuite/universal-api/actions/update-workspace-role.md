# KiteSuite: Update Workspace Role

Updates an existing workspace role in KiteSuite.

```
PUT https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/update-workspace-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KiteSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/update-workspace-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "roleName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/update-workspace-role', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "roleName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Workspace role ID. |
| `roleName` | string | yes | Updated workspace role name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "isDefault": true,
      "roleName": "Ava Chen",
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `isDefault` | boolean |  |
| `roleName` | string |  |
| `workspace` | string |  |

## Native endpoint

Through the native KiteSuite API, this operation is `PATCH /api/v1/workspace-role/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-workspace-role.md) for the provider-specific parameters and requirements.

