# Range: Create Team

Create a new team with optional parent and mascot.

```
POST https://connect.mindcloud.co/v1/universal/range/latest/actions/create-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Range `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/range/latest/actions/create-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/range/latest/actions/create-team', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | The team's charter or purpose. |
| `mascot` | string | no | An emoji-one code such as :bear:. |
| `name` | string | no | The team's name. |
| `parentId` | string | no | Parent team ID. Leave empty for a root team. |
| `slug` | string | no | Unique URL slug for the team. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archivedAt": "string",
      "createdAt": "string",
      "description": "string",
      "linkHref1": "https://example.com",
      "linkHref2": "https://example.com",
      "linkHref3": "https://example.com",
      "linkText1": "https://example.com",
      "linkText2": "https://example.com",
      "linkText3": "https://example.com",
      "mascot": "string",
      "memberPolicy": "string",
      "name": "Ava Chen",
      "onboardedAt": "string",
      "orgId": "string",
      "parentId": "string",
      "promptsState": "string",
      "relations": [
        {}
      ],
      "slug": "string",
      "teamId": "string",
      "workflowId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archivedAt` | string |  |
| `createdAt` | string |  |
| `description` | string |  |
| `linkHref1` | string |  |
| `linkHref2` | string |  |
| `linkHref3` | string |  |
| `linkText1` | string |  |
| `linkText2` | string |  |
| `linkText3` | string |  |
| `mascot` | string |  |
| `memberPolicy` | string |  |
| `name` | string |  |
| `onboardedAt` | string |  |
| `orgId` | string |  |
| `parentId` | string |  |
| `promptsState` | string |  |
| `relations` | array<object> |  |
| `slug` | string |  |
| `teamId` | string |  |
| `workflowId` | string |  |

## Native endpoint

Through the native Range API, this operation is `POST /v1/teams` (base URL `https://api.range.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-team.md) for the provider-specific parameters and requirements.

