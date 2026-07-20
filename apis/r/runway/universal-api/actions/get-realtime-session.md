# Runway: Get Realtime Session

Retrieves a realtime session from Runway.

```
GET https://connect.mindcloud.co/v1/universal/runway/latest/actions/get-realtime-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runway/latest/actions/get-realtime-session?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runway/latest/actions/get-realtime-session?${params}`, {
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
| `id` | string | yes | UUID of the realtime session to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientSecret": "string",
      "createdAt": "string",
      "error": "string",
      "id": "string",
      "status": "string",
      "updatedAt": "string",
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
| `createdAt` | string |  |
| `error` | string |  |
| `id` | string |  |
| `status` | string |  |
| `updatedAt` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Runway API, this operation is `GET /v1/realtime_sessions/[:id]` (base URL `https://api.dev.runwayml.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-realtime-session.md) for the provider-specific parameters and requirements.

