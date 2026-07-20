# Supabase: Delete Bucket

Deletes a storage bucket from your Supabase project.

```
DELETE https://connect.mindcloud.co/v1/universal/supabase/latest/actions/delete-bucket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Supabase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/supabase/latest/actions/delete-bucket?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/supabase/latest/actions/delete-bucket?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
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

Through the native Supabase API, this operation is `DELETE /storage/v1/bucket/:bucketId` (base URL `{{credentials.projectUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-bucket.md) for the provider-specific parameters and requirements.

