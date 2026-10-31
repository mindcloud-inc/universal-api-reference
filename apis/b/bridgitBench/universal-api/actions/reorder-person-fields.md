# Bridgit Bench: Reorder Person Fields



```
PUT https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/reorder-person-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/reorder-person-fields" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "payload[]": [
    {}
  ],
  "payload[].fieldId": 1,
  "payload[].displayOrder": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/reorder-person-fields', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "payload[]": [{}],
    "payload[].fieldId": 1,
    "payload[].displayOrder": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The account ID |
| `payload[]` | array<object> | yes |  |
| `payload[].fieldId` | number | yes | The field ID to reorder |
| `payload[].displayOrder` | number | yes | The new display order position (1-indexed) |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `PUT /rp/api/v1/accounts/:id/person-fields/_reorder` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reorder-person-fields.md) for the provider-specific parameters and requirements.

