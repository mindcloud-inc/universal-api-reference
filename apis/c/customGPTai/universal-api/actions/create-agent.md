# CustomGPT.ai: Create Agent

Creates a new agent in CustomGPT.ai.

```
POST https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/create-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomGPT.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/create-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectName": "Ava Chen",
  "sitemapPath": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/create-agent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectName": "Ava Chen",
    "sitemapPath": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectName` | string | yes | Name for the temporary agent used during pagination remediation. |
| `sitemapPath` | string | yes | Source URL used to initialize the temporary agent. |

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

Through the native CustomGPT.ai API, this operation is `POST /projects` (base URL `https://app.customgpt.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-agent.md) for the provider-specific parameters and requirements.

