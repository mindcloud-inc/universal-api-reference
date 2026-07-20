# Supabase: Update Bucket

Updates a storage bucket in your Supabase project.

```
PUT https://connect.mindcloud.co/v1/universal/supabase/latest/actions/update-bucket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Supabase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/supabase/latest/actions/update-bucket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/supabase/latest/actions/update-bucket', {
  method: 'PUT',
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

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Supabase API, this operation is `PUT /storage/v1/bucket/:bucketId` (base URL `{{credentials.projectUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-bucket.md) for the provider-specific parameters and requirements.

