# Typebot: Get Result



```
GET https://connect.mindcloud.co/v1/universal/typebot/latest/actions/get-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typebot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typebot/latest/actions/get-result?connectionId=$CONNECTION_ID&typebotId=string&resultId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "typebotId": "string",
  "resultId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typebot/latest/actions/get-result?${params}`, {
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
| `typebotId` | string | yes | The Typebot ID. |
| `resultId` | string | yes | The result ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answers": [
        {
          "attachedFileUrls": [
            "https://example.com"
          ],
          "blockId": "string",
          "content": "string"
        }
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "hasStarted": true,
      "id": "string",
      "isArchived": true,
      "isCompleted": true,
      "lastChatSessionId": "string",
      "typebotId": "string",
      "variables": [
        {
          "id": "string",
          "isSessionVariable": true,
          "name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answers[].attachedFileUrls` | array<string> |  |
| `answers[].blockId` | string |  |
| `answers[].content` | string |  |
| `createdAt` | date |  |
| `hasStarted` | boolean |  |
| `id` | string |  |
| `isArchived` | boolean |  |
| `isCompleted` | boolean |  |
| `lastChatSessionId` | string |  |
| `typebotId` | string |  |
| `variables[].id` | string |  |
| `variables[].isSessionVariable` | boolean |  |
| `variables[].name` | string |  |

## Native endpoint

Through the native Typebot API, this operation is `GET /v1/typebots/:typebotId/results/:resultId` (base URL `https://app.typebot.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-result.md) for the provider-specific parameters and requirements.

