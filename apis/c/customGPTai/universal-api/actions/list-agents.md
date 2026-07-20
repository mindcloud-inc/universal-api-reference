# CustomGPT.ai: List Agents

Retrieves all agents from your CustomGPT.ai account.

```
GET https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/list-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomGPT.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/list-agents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/list-agents?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "areLicensesAllowed": true,
      "createdAt": "string",
      "deletedAt": "string",
      "id": 1,
      "isChatActive": true,
      "isShared": true,
      "projectName": "Ava Chen",
      "sitemapPath": "string",
      "teamId": 1,
      "type": "string",
      "updatedAt": "string",
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
| `createdAt` | string |  |
| `deletedAt` | string |  |
| `id` | number |  |
| `isChatActive` | boolean |  |
| `isShared` | boolean |  |
| `projectName` | string |  |
| `sitemapPath` | string |  |
| `teamId` | number |  |
| `type` | string |  |
| `updatedAt` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native CustomGPT.ai API, this operation is `GET /projects` (base URL `https://app.customgpt.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-agents.md) for the provider-specific parameters and requirements.

