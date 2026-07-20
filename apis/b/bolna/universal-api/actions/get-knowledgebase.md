# Bolna: Get Knowledgebase

Retrieves a specific knowledgebase from your Bolna account.

```
GET https://connect.mindcloud.co/v1/universal/bolna/latest/actions/get-knowledgebase
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bolna `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bolna/latest/actions/get-knowledgebase?connectionId=$CONNECTION_ID&ragId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ragId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bolna/latest/actions/get-knowledgebase?${params}`, {
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
| `ragId` | string | yes | The unique knowledgebase ID from Bolna. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentCount": 1,
      "chunkSize": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fileName": "Ava Chen",
      "humanizedCreatedAt": "string",
      "isUsedByAgents": true,
      "languageSupport": "string",
      "overlapping": 1,
      "ragId": "string",
      "similarityTopK": 1,
      "source": "string",
      "sourceType": "string",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "vectorId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentCount` | number |  |
| `chunkSize` | number |  |
| `createdAt` | date |  |
| `fileName` | string |  |
| `humanizedCreatedAt` | string |  |
| `isUsedByAgents` | boolean |  |
| `languageSupport` | string |  |
| `overlapping` | number |  |
| `ragId` | string |  |
| `similarityTopK` | number |  |
| `source` | string |  |
| `sourceType` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |
| `vectorId` | string |  |

## Native endpoint

Through the native Bolna API, this operation is `GET /knowledgebase/:ragId` (base URL `https://api.bolna.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-knowledgebase.md) for the provider-specific parameters and requirements.

