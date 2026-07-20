# Runway: Create Realtime Session

Creates a realtime session in Runway.

```
POST https://connect.mindcloud.co/v1/universal/runway/latest/actions/create-realtime-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/runway/latest/actions/create-realtime-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "avatar": {},
  "model": "gwm1_avatars"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/runway/latest/actions/create-realtime-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "avatar": {},
    "model": "gwm1_avatars"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `avatar` | object | yes | Avatar object using a runway-preset or custom avatar id. |
| `maxDuration` | number | no | Maximum session duration in seconds, between 10 and 300. Default: `300`. |
| `model` | string | yes | Runway currently requires gwm1_avatars. Default: `gwm1_avatars`. |
| `personality` | string | no | Optional session personality override. |
| `startScript` | string | no | Optional opening script override for the session. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientSecret": "string",
      "error": "string",
      "id": "string",
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientSecret` | string |  |
| `error` | string |  |
| `id` | string |  |
| `status` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Runway API, this operation is `POST /v1/realtime_sessions` (base URL `https://api.dev.runwayml.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-realtime-session.md) for the provider-specific parameters and requirements.

