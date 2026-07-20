# Airtop: Create Window

Creates a new browser window in Airtop.

```
POST https://connect.mindcloud.co/v1/universal/airtop/latest/actions/create-window
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airtop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/airtop/latest/actions/create-window" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sessionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airtop/latest/actions/create-window', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sessionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sessionId` | string | yes |  |
| `url` | string | no |  |
| `waitUntil` | string | no |  |
| `screenResolution` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Airtop API returns.

## Native endpoint

Through the native Airtop API, this operation is `POST /sessions/:sessionId/windows` (base URL `https://api.airtop.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-window.md) for the provider-specific parameters and requirements.

