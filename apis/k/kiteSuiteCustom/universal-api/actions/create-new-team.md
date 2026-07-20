# Kite Suite: Create new Team



```
POST https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/create-new-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/create-new-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "name": "Ava Chen",
  "description": "string",
  "members[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/create-new-team', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "name": "Ava Chen",
    "description": "string",
    "members[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | Request body |
| `name` | string | yes |  |
| `description` | string | yes |  |
| `members[]` | array | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "createdAt": "string",
      "createdBy": "string",
      "description": "string",
      "isTrashed": true,
      "members": [
        "string"
      ],
      "name": "Ava Chen",
      "updatedAt": "string",
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | ID of the Team |
| `createdAt` | string | Team creation date |
| `createdBy` | string | User ID of creator |
| `description` | string | Description of the Team |
| `isTrashed` | boolean | Trash status of the Team |
| `members` | array<string> | List of team members (user references) |
| `name` | string | Name of the Team |
| `updatedAt` | string | Last update date |
| `workspace` | string | Workspace ID this team belongs to |

## Native endpoint

Through the native Kite Suite API, this operation is `POST /api/v1/team` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-new-team.md) for the provider-specific parameters and requirements.

