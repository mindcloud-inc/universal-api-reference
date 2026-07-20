# Insightful: Update Team

Updates an existing team in your Insightful account.

```
PUT https://connect.mindcloud.co/v1/universal/insightful/latest/actions/update-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insightful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/insightful/latest/actions/update-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/insightful/latest/actions/update-team', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | The updated team description. |
| `employees[]` | array<string> | no | Employee IDs to assign to the team. |
| `id` | string | yes | The team ID to update. |
| `ignoreNeutral` | boolean | no | Whether to ignore neutral applications for the team. |
| `ignoreProductive` | boolean | no | Whether to ignore productive applications for the team. |
| `ignoreUnproductive` | boolean | no | Whether to ignore unproductive applications for the team. |
| `ignoreUnreviewed` | boolean | no | Whether to ignore unreviewed applications for the team. |
| `projects[]` | array<string> | no | Project IDs to assign to the team. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "default": true,
      "description": "string",
      "id": "string",
      "ignoreNeutral": true,
      "ignoreProductive": true,
      "ignoreUnproductive": true,
      "ignoreUnreviewed": true,
      "modelName": "Ava Chen",
      "name": "Ava Chen",
      "organizationId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `default` | boolean |  |
| `description` | string |  |
| `id` | string |  |
| `ignoreNeutral` | boolean |  |
| `ignoreProductive` | boolean |  |
| `ignoreUnproductive` | boolean |  |
| `ignoreUnreviewed` | boolean |  |
| `modelName` | string |  |
| `name` | string |  |
| `organizationId` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Insightful API, this operation is `PUT /team/:id` (base URL `https://app.insightful.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-team.md) for the provider-specific parameters and requirements.

