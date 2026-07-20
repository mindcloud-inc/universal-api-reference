# KiteSuite: Update Project Member Role

Updates a project member role in KiteSuite.

```
PUT https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/update-project-member-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KiteSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/update-project-member-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "projectID": "string",
  "roleID": "e.g. 69d3e6b9353b6b2d2a539a11"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/update-project-member-role', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "projectID": "string",
    "roleID": "e.g. 69d3e6b9353b6b2d2a539a11"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Runtime expects the user ID for the project member. |
| `projectID` | string | yes | Project ID. |
| `roleID` | string | yes | Project role ID to assign. Example: `e.g. 69d3e6b9353b6b2d2a539a11`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "active": true,
      "member": {},
      "role": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `active` | boolean |  |
| `member` | object |  |
| `role` | object |  |

## Native endpoint

Through the native KiteSuite API, this operation is `PATCH /api/v1/project/member/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project-member-role.md) for the provider-specific parameters and requirements.

