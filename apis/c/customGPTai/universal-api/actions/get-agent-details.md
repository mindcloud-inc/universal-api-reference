# CustomGPT.ai: Get Agent Details

Retrieves detailed agent information from CustomGPT.ai.

```
GET https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/get-agent-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomGPT.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/get-agent-details?connectionId=$CONNECTION_ID&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/get-agent-details?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes | The project ID of the agent to retrieve. |

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

Through the native CustomGPT.ai API, this operation is `GET /projects/:projectId` (base URL `https://app.customgpt.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent-details.md) for the provider-specific parameters and requirements.

