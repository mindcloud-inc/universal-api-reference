# Productlane: Update Doc Group

Updates a doc group in your Productlane help center.

```
PUT https://connect.mindcloud.co/v1/universal/productlane/latest/actions/update-doc-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productlane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/productlane/latest/actions/update-doc-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "a48ae618-61e4-4ec1-b23a-56ac476c95d5"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/productlane/latest/actions/update-doc-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "a48ae618-61e4-4ec1-b23a-56ac476c95d5"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Doc group ID. Example: `a48ae618-61e4-4ec1-b23a-56ac476c95d5`. |
| `name` | string | no | Updated docs group name. Example: `Stage 3 Docs Group Updated`. |
| `order` | number | no | Display order for the group. Example: `1`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Productlane API returns.

## Native endpoint

Through the native Productlane API, this operation is `PATCH /docs/groups/{id}` (base URL `https://productlane.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-doc-group.md) for the provider-specific parameters and requirements.

