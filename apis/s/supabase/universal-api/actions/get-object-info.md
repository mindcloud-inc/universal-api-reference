# Supabase: Get Object Info

Retrieves object details from a Supabase storage bucket.

```
GET https://connect.mindcloud.co/v1/universal/supabase/latest/actions/get-object-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Supabase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/supabase/latest/actions/get-object-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/supabase/latest/actions/get-object-info?${params}`, {
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
      "metadata": {},
      "name": "Ava Chen",
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
| `metadata` | object |  |
| `name` | string |  |
| `updatedAt` | date |  |
| `userMetadata` | object |  |
| `version` | string |  |

## Native endpoint

Through the native Supabase API, this operation is `GET /storage/v1/object/info/:bucketName/:objectPath` (base URL `{{credentials.projectUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-object-info.md) for the provider-specific parameters and requirements.

