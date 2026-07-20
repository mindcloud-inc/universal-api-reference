# Feedbin: Create Saved Search

Creates a new saved search in Feedbin.

```
POST https://connect.mindcloud.co/v1/universal/feedbin/latest/actions/create-saved-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feedbin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/feedbin/latest/actions/create-saved-search" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "query": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/feedbin/latest/actions/create-saved-search', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "query": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Saved search name. |
| `query` | string | yes | Feedbin saved search query, for example javascript is:unread. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "query": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |
| `query` | string |  |

## Native endpoint

Through the native Feedbin API, this operation is `POST saved_searches.json` (base URL `https://api.feedbin.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-saved-search.md) for the provider-specific parameters and requirements.

