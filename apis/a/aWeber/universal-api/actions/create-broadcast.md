# AWeber: Create Broadcast

Creates a new broadcast in AWeber.

```
POST https://connect.mindcloud.co/v1/universal/aWeber/latest/actions/create-broadcast
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AWeber `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aWeber/latest/actions/create-broadcast" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string",
  "bodyHtml": "string",
  "bodyText": "string",
  "listId": "string",
  "subject": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aWeber/latest/actions/create-broadcast', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string",
    "bodyHtml": "string",
    "bodyText": "string",
    "listId": "string",
    "subject": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes |  |
| `bodyAmp` | string | no |  |
| `bodyHtml` | string | yes |  |
| `bodyText` | string | yes |  |
| `clickTrackingEnabled` | boolean | no |  |
| `excludeLists` | string | no |  |
| `facebookIntegration` | string | no |  |
| `includeLists` | string | no |  |
| `isArchived` | boolean | no |  |
| `listId` | string | yes |  |
| `notifyOnSend` | boolean | no |  |
| `segmentLink` | string | no |  |
| `subject` | string | yes |  |
| `twitterIntegration` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AWeber API returns.

## Native endpoint

Through the native AWeber API, this operation is `POST /accounts/:accountId/lists/:listId/broadcasts` (base URL `https://api.aweber.com/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-broadcast.md) for the provider-specific parameters and requirements.

