# CustomGPT.ai: Update Agent

Updates an existing agent in CustomGPT.ai.

```
PUT https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/update-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomGPT.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/update-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "projectName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/update-agent', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "projectName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes | The project ID of the agent to update. |
| `projectName` | string | yes | The updated name for the agent. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "areLicensesAllowed": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "isChatActive": true,
      "isShared": true,
      "projectName": "Ava Chen",
      "sitemapPath": "string",
      "teamId": 1,
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `areLicensesAllowed` | boolean |  |
| `createdAt` | date |  |
| `deletedAt` | date |  |
| `id` | number |  |
| `isChatActive` | boolean |  |
| `isShared` | boolean |  |
| `projectName` | string |  |
| `sitemapPath` | string |  |
| `teamId` | number |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `userId` | number |  |

## Native endpoint

Through the native CustomGPT.ai API, this operation is `POST /projects/:projectId` (base URL `https://app.customgpt.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-agent.md) for the provider-specific parameters and requirements.

