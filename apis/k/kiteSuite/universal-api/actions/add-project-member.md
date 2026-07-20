# KiteSuite: Add Project Member

Adds a member to a project in KiteSuite.

```
POST https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/add-project-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KiteSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/add-project-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectID": "string",
  "members[]": [
    "string"
  ],
  "roleID": "e.g. 69d3e6b9353b6b2d2a539a11"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/add-project-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectID": "string",
    "members[]": ["string"],
    "roleID": "e.g. 69d3e6b9353b6b2d2a539a11"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectID` | string | yes | Project ID. |
| `members[]` | array<string> | yes | Email addresses to add to the project. Pass an array of emails. Accepts multiple values as an array. |
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

Through the native KiteSuite API, this operation is `POST /api/v1/project/member` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-project-member.md) for the provider-specific parameters and requirements.

