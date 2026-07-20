# RocketReach: Bulk Lookup Universal People

Creates a RocketReach Universal bulk people lookup.

```
POST https://connect.mindcloud.co/v1/universal/rocketReach/latest/actions/bulk-lookup-universal-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RocketReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rocketReach/latest/actions/bulk-lookup-universal-people" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rocketReach/latest/actions/bulk-lookup-universal-people', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `queries` | list<object> | no | Up to 100 person lookup query objects to submit in one bulk request. Example: `[object Object]`. |
| `profileList` | string | no | Add specified contacts to this profile list. Default: `API Bulk Lookup`. Example: `API Bulk Lookup`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhookId` | number | no | Webhook ID to post lookup results when the bulk job completes. Example: `12345`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RocketReach API returns.

## Native endpoint

Through the native RocketReach API, this operation is `POST /universal/person/bulk_lookup` (base URL `https://api.rocketreach.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-lookup-universal-people.md) for the provider-specific parameters and requirements.

