# OnlineCheckWriter: Void Check

Voids a specific check.

```
PUT https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/void-check
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnlineCheckWriter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/void-check" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "checkId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/void-check', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "checkId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `checkId` | string | yes | The check identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OnlineCheckWriter API returns.

## Native endpoint

Through the native OnlineCheckWriter API, this operation is `POST /checks/:checkId/void` (base URL `https://test.onlinecheckwriter.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/void-check.md) for the provider-specific parameters and requirements.

