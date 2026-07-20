# Typebot: Get Result Transcript



```
GET https://connect.mindcloud.co/v1/universal/typebot/latest/actions/get-result-transcript
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typebot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typebot/latest/actions/get-result-transcript?connectionId=$CONNECTION_ID&typebotId=string&resultId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "typebotId": "string",
  "resultId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typebot/latest/actions/get-result-transcript?${params}`, {
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
      "audio": "string",
      "image": "string",
      "role": "string",
      "text": "string",
      "type": "string",
      "video": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audio` | string |  |
| `image` | string |  |
| `role` | string |  |
| `text` | string |  |
| `type` | string |  |
| `video` | string |  |

## Native endpoint

Through the native Typebot API, this operation is `GET /v1/typebots/:typebotId/results/:resultId/transcript` (base URL `https://app.typebot.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-result-transcript.md) for the provider-specific parameters and requirements.

