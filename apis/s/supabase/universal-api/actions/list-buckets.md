# Supabase: List Buckets

Retrieves storage buckets from your Supabase project.

```
GET https://connect.mindcloud.co/v1/universal/supabase/latest/actions/list-buckets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Supabase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/supabase/latest/actions/list-buckets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/supabase/latest/actions/list-buckets?${params}`, {
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
      "allowedMimeTypes": [
        "string"
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fileSizeLimit": 1,
      "id": "string",
      "name": "Ava Chen",
      "owner": "string",
      "public": true,
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowedMimeTypes` | array<string> |  |
| `createdAt` | date |  |
| `fileSizeLimit` | number |  |
| `id` | string |  |
| `name` | string |  |
| `owner` | string |  |
| `public` | boolean |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Supabase API, this operation is `GET /storage/v1/bucket` (base URL `{{credentials.projectUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-buckets.md) for the provider-specific parameters and requirements.

