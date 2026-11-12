# Geotab: Create Asset Group



```
POST https://connect.mindcloud.co/v1/universal/geotab/latest/actions/create-asset-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geotab `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/geotab/latest/actions/create-asset-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entity": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/geotab/latest/actions/create-asset-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entity": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entity` | object | yes | Complete Group entity to add. Include the parent group relationship required by MyGeotab. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Geotab API returns.

## Native endpoint

Through the native Geotab API, this operation is `POST` (base URL `https://{{credentials.server}}/apiv1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-asset-group.md) for the provider-specific parameters and requirements.

