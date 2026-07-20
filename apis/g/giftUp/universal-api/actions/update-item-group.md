# Gift Up: Update Item Group



```
PUT https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/update-item-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gift Up `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/update-item-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "ae7edb66-dc47-49c3-2a05-08de85d65fe3",
  "operations[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/update-item-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "ae7edb66-dc47-49c3-2a05-08de85d65fe3",
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
| `id` | string | yes | Example: `ae7edb66-dc47-49c3-2a05-08de85d65fe3`. |
| `operations[]` | array<object> | yes | JSON Patch operations to apply to the item group. |
| `operations[]` | array<object> | yes | JSON Patch operations to apply to the item group. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Gift Up API returns.

## Native endpoint

Through the native Gift Up API, this operation is `PATCH /groups/:id` (base URL `https://api.giftup.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-item-group.md) for the provider-specific parameters and requirements.

