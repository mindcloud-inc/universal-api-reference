# Supabase: Delete Objects

Deletes multiple objects from a Supabase storage bucket.

```
DELETE https://connect.mindcloud.co/v1/universal/supabase/latest/actions/delete-objects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Supabase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/supabase/latest/actions/delete-objects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/supabase/latest/actions/delete-objects?${params}`, {
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
      "bucketId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "lastAccessedAt": "2026-05-07T12:00:00.000Z",
      "metadata": {},
      "name": "Ava Chen",
      "owner": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userMetadata": {},
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bucketId` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `lastAccessedAt` | date |  |
| `metadata` | object |  |
| `name` | string |  |
| `owner` | string |  |
| `updatedAt` | date |  |
| `userMetadata` | object |  |
| `version` | string |  |

## Native endpoint

Through the native Supabase API, this operation is `DELETE /storage/v1/object/:bucketName` (base URL `{{credentials.projectUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-objects.md) for the provider-specific parameters and requirements.

