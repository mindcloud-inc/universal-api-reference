# Supabase: Insert Rows (Bulk)

Creates multiple rows in a Supabase table.

```
POST https://connect.mindcloud.co/v1/universal/supabase/latest/actions/insert-rows-bulk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Supabase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/supabase/latest/actions/insert-rows-bulk" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/supabase/latest/actions/insert-rows-bulk', {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Supabase API returns.

## Native endpoint

Through the native Supabase API, this operation is `POST /rest/v1/:table` (base URL `{{credentials.projectUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-rows-bulk.md) for the provider-specific parameters and requirements.

