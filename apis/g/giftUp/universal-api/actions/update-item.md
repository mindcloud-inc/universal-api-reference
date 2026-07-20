# Gift Up: Update Item



```
PUT https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/update-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gift Up `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/update-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "31adf07f-24e1-445d-33fe-08de85d66079",
  "operations[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/update-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "31adf07f-24e1-445d-33fe-08de85d66079",
    "operations[]": [{}],
    "operations[]": [{}],
    "operations[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Example: `31adf07f-24e1-445d-33fe-08de85d66079`. |
| `operations[]` | array<object> | yes | JSON Patch operations to apply to the item. |
| `operations[]` | array<object> | yes | JSON Patch operations to apply to the item. |
| `operations[]` | array<object> | yes | JSON Patch operations to apply to the item. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Gift Up API returns.

## Native endpoint

Through the native Gift Up API, this operation is `PATCH /items/:id` (base URL `https://api.giftup.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-item.md) for the provider-specific parameters and requirements.

