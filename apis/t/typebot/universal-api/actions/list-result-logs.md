# Typebot: List Result Logs



```
GET https://connect.mindcloud.co/v1/universal/typebot/latest/actions/list-result-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typebot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typebot/latest/actions/list-result-logs?connectionId=$CONNECTION_ID&typebotId=string&resultId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "typebotId": "string",
  "resultId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typebot/latest/actions/list-result-logs?${params}`, {
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
      "context": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "details": "string",
      "id": "string",
      "resultId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `context` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `details` | string |  |
| `id` | string |  |
| `resultId` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Typebot API, this operation is `GET /v1/typebots/:typebotId/results/:resultId/logs` (base URL `https://app.typebot.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-result-logs.md) for the provider-specific parameters and requirements.

