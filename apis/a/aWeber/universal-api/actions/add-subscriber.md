# AWeber: Add Subscriber

Creates a new subscriber in AWeber.

```
POST https://connect.mindcloud.co/v1/universal/aWeber/latest/actions/add-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AWeber `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aWeber/latest/actions/add-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string",
  "email": "ava@example.com",
  "listId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aWeber/latest/actions/add-subscriber', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string",
    "email": "ava@example.com",
    "listId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes |  |
| `adTracking` | string | no |  |
| `customFields` | object | no |  |
| `email` | string | yes |  |
| `ipAddress` | string | no |  |
| `lastFollowupMessageNumberSent` | number | no |  |
| `listId` | string | yes |  |
| `miscNotes` | string | no |  |
| `name` | string | no |  |
| `strictCustomFields` | string | no |  |
| `tags[]` | array<string> | no |  |
| `updateExisting` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AWeber API returns.

## Native endpoint

Through the native AWeber API, this operation is `POST /accounts/:accountId/lists/:listId/subscribers` (base URL `https://api.aweber.com/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-subscriber.md) for the provider-specific parameters and requirements.

