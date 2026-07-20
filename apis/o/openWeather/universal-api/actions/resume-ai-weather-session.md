# OpenWeather: Resume AI Weather Session

Continues an OpenWeather AI weather assistant session.

```
PUT https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/resume-ai-weather-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/resume-ai-weather-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sessionId": "string",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/resume-ai-weather-session', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sessionId": "string",
    "prompt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sessionId` | string | yes | AI assistant session identifier. |
| `prompt` | string | yes | Follow-up weather-related question. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answer": "string",
      "data": {},
      "session_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answer` | string |  |
| `data` | object |  |
| `session_id` | string |  |

## Native endpoint

Through the native OpenWeather API, this operation is `POST /assistant/session/:sessionId` (base URL `https://api.openweathermap.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resume-ai-weather-session.md) for the provider-specific parameters and requirements.

