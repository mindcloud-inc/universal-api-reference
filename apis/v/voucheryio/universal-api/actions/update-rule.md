# Vouchery.io: Update Rule



```
PUT https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/update-rule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vouchery.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/update-rule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "operator": "string",
  "type": "string",
  "value": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/update-rule', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "operator": "string",
    "type": "string",
    "value": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Rule ID from Vouchery. |
| `operator` | string | yes | Rule operator. |
| `type` | string | yes | Rule type discriminator for update. |
| `value` | number | yes | Rule value. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vouchery.io API returns.

## Native endpoint

Through the native Vouchery.io API, this operation is `PUT /rules/:id` (base URL `https://mindcloud.sandbox.vouchery.app/api/v2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-rule.md) for the provider-specific parameters and requirements.

