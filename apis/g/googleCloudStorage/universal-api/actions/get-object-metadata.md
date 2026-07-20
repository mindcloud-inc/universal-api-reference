# Google Cloud Storage: Get Object Metadata

Retrieves object metadata from Google Cloud Storage.

```
GET https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/get-object-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Storage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/get-object-metadata?connectionId=$CONNECTION_ID&bucket=string&object=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bucket": "string",
  "object": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/get-object-metadata?${params}`, {
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
| `bucket` | list<string> | yes | Bucket name. |
| `object` | string | yes | Object name. |

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

Through the native Google Cloud Storage API, this operation is `GET /storage/v1/b/:bucket/o/:object` (base URL `https://storage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-object-metadata.md) for the provider-specific parameters and requirements.

