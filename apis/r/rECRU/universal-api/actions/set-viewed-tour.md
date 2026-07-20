# RECRU: Set Viewed Tour



```
PUT https://connect.mindcloud.co/v1/universal/rECRU/latest/actions/set-viewed-tour
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RECRU `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rECRU/latest/actions/set-viewed-tour" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tourId": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rECRU/latest/actions/set-viewed-tour', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tourId": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tourId` | number | yes | Default: `1`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RECRU API returns.

## Native endpoint

Through the native RECRU API, this operation is `POST` (base URL `https://mindclo.recru.eu/api/json-rpc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-viewed-tour.md) for the provider-specific parameters and requirements.

