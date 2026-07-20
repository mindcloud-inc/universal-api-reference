# LogSnag: Track Page View



```
POST https://connect.mindcloud.co/v1/universal/logSnag/latest/actions/track-page-view
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LogSnag `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/logSnag/latest/actions/track-page-view" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project": "string",
  "userId": "string",
  "payload": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logSnag/latest/actions/track-page-view', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project": "string",
    "userId": "string",
    "payload": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project` | string | yes | Project name in LogSnag. |
| `userId` | string | yes | User identifier for the page event. |
| `payload` | object | yes | Page payload object. Includes path and optional metadata. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "payload": {
        "path": "string",
        "referrer": "string",
        "title": "string"
      },
      "project": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `payload.path` | string | Tracked page path. |
| `payload.referrer` | string | Tracked page referrer. |
| `payload.title` | string | Tracked page title. |
| `project` | string | LogSnag project name. |
| `userId` | string | User identifier for the page event. |

## Native endpoint

Through the native LogSnag API, this operation is `POST /page` (base URL `https://api.logsnag.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/track-page-view.md) for the provider-specific parameters and requirements.

