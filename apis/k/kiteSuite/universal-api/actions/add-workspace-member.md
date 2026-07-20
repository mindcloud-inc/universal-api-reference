# KiteSuite: Add Workspace Member

Adds a member to a workspace in KiteSuite.

```
POST https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/add-workspace-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KiteSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/add-workspace-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "members[]": [
    "string"
  ],
  "role": "e.g. 69cfacd46d907abc77fcc550"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/add-workspace-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "members[]": ["string"],
    "role": "e.g. 69cfacd46d907abc77fcc550"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `members[]` | array<string> | yes | Email addresses to invite to the workspace. Pass an array of emails. Accepts multiple values as an array. |
| `role` | string | yes | Workspace role ID to assign. Example: `e.g. 69cfacd46d907abc77fcc550`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "email": "ava@example.com",
      "fullName": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `email` | string |  |
| `fullName` | string |  |
| `status` | string |  |

## Native endpoint

Through the native KiteSuite API, this operation is `POST /api/v1/workspace/member` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-workspace-member.md) for the provider-specific parameters and requirements.

