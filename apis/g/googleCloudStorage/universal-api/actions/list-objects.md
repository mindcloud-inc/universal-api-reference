# Google Cloud Storage: List Objects

Retrieves a list of objects from Google Cloud Storage.

```
GET https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/list-objects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Storage `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/list-objects?connectionId=$CONNECTION_ID&limit=25&offset=0&bucket=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "bucket": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/list-objects?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bucket` | list<string> | yes | Bucket to list objects from. |
| `prefix` | string | no | Return objects whose names begin with this prefix. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `delimiter` | string | no | Delimiter used to emulate directory-style listings. |
| `matchGlob` | string | no | Glob pattern for object names. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bucket": "string",
      "contentType": "string",
      "generation": "string",
      "id": "string",
      "mediaLink": "https://example.com",
      "metageneration": "string",
      "name": "Ava Chen",
      "size": "string",
      "timeCreated": "2026-05-07T12:00:00.000Z",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bucket` | string |  |
| `contentType` | string |  |
| `generation` | string |  |
| `id` | string |  |
| `mediaLink` | string |  |
| `metageneration` | string |  |
| `name` | string |  |
| `size` | string |  |
| `timeCreated` | date |  |
| `updated` | date |  |

## Native endpoint

Through the native Google Cloud Storage API, this operation is `GET /storage/v1/b/:bucket/o` (base URL `https://storage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-objects.md) for the provider-specific parameters and requirements.

