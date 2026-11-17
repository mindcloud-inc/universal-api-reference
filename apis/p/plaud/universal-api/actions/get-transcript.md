# Plaud AI: Get Transcript



```
GET https://connect.mindcloud.co/v1/universal/plaud/latest/actions/get-transcript
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Plaud AI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/plaud/latest/actions/get-transcript?connectionId=$CONNECTION_ID&limit=25&offset=0&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/plaud/latest/actions/get-transcript?${params}`, {
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
| `fileId` | list<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "endTime": 1,
      "originalSpeaker": "string",
      "speaker": "string",
      "startTime": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string |  |
| `endTime` | number |  |
| `originalSpeaker` | string |  |
| `speaker` | string |  |
| `startTime` | number |  |

## Native endpoint

Through the native Plaud AI API, this operation is `POST /mcp` (base URL `https://mcp.plaud.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-transcript.md) for the provider-specific parameters and requirements.

