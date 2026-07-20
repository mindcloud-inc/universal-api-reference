# Dovetail: Update Doc

Updates an existing doc in Dovetail.

```
PUT https://connect.mindcloud.co/v1/universal/dovetail/latest/actions/update-doc
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dovetail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dovetail/latest/actions/update-doc" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "docId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dovetail/latest/actions/update-doc', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "docId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `docId` | string | yes |  |
| `title` | string | no | Doc title. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dovetail API returns.

## Native endpoint

Through the native Dovetail API, this operation is `PATCH /v1/docs/:docId` (base URL `https://dovetail.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-doc.md) for the provider-specific parameters and requirements.

