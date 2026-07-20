# Feedbin: Mark Entries Read

Marks entries as read in Feedbin.

```
PUT https://connect.mindcloud.co/v1/universal/feedbin/latest/actions/mark-entries-read
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feedbin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/feedbin/latest/actions/mark-entries-read" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "unreadEntries": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/feedbin/latest/actions/mark-entries-read', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "unreadEntries": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `unreadEntries` | number<number> | yes | Entry IDs to mark read. Feedbin allows up to 1,000 IDs per request. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native Feedbin API, this operation is `DELETE unread_entries.json` (base URL `https://api.feedbin.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-entries-read.md) for the provider-specific parameters and requirements.

