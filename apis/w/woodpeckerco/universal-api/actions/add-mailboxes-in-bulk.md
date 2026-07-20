# Woodpecker.co: Add Mailboxes In Bulk

Creates one or more mailboxes in Woodpecker.

```
POST https://connect.mindcloud.co/v1/universal/woodpeckerco/latest/actions/add-mailboxes-in-bulk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Woodpecker.co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/woodpeckerco/latest/actions/add-mailboxes-in-bulk" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/woodpeckerco/latest/actions/add-mailboxes-in-bulk', {
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



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Woodpecker.co API returns.

## Native endpoint

Through the native Woodpecker.co API, this operation is `POST /rest/v2/mailboxes/manual_connection/bulk` (base URL `https://api.woodpecker.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-mailboxes-in-bulk.md) for the provider-specific parameters and requirements.

