# FTrack: Export Review Session Feedback

Creates a review session feedback export in FTrack.

```
POST https://connect.mindcloud.co/v1/universal/fTrack/latest/actions/export-review-session-feedback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FTrack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fTrack/latest/actions/export-review-session-feedback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "reviewSessionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fTrack/latest/actions/export-review-session-feedback', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "reviewSessionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reviewSessionId` | string | yes | Review session whose feedback should be exported. |
| `language` | string | no | Optional export language. Default: `en`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native FTrack API returns.

## Native endpoint

Through the native FTrack API, this operation is `POST /api` (base URL `{{credentials.serverUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-review-session-feedback.md) for the provider-specific parameters and requirements.

