# Retell AI: List Retell LLMs

Retrieves Retell LLMs from Retell AI.

```
GET https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/list-retell-llms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Retell AI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/list-retell-llms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/list-retell-llms?${params}`, {
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
| `paginationKeyVersion` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "generalPrompt": "string",
      "generalTools": [
        [
          {}
        ]
      ],
      "isPublished": true,
      "lastModificationTimestamp": 1,
      "llmId": "string",
      "model": "string",
      "startSpeaker": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `generalPrompt` | string |  |
| `generalTools[]` | array<object> |  |
| `generalTools[].description` | string |  |
| `generalTools[].name` | string |  |
| `generalTools[].transferDestination` | object |  |
| `generalTools[].transferDestination.number` | string |  |
| `generalTools[].transferDestination.type` | string |  |
| `generalTools[].transferOption` | object |  |
| `generalTools[].transferOption.coldTransferMode` | string |  |
| `generalTools[].transferOption.type` | string |  |
| `generalTools[].type` | string |  |
| `isPublished` | boolean |  |
| `lastModificationTimestamp` | number |  |
| `llmId` | string |  |
| `model` | string |  |
| `startSpeaker` | string |  |
| `version` | number |  |

## Native endpoint

Through the native Retell AI API, this operation is `GET /list-retell-llms` (base URL `https://api.retellai.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-retell-llms.md) for the provider-specific parameters and requirements.

