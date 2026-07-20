# Google Cloud Storage: List Buckets

Retrieves a list of buckets from Google Cloud Storage.

```
GET https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/list-buckets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Storage `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/list-buckets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/list-buckets?${params}`, {
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
| `prefix` | string | no | Optional bucket name prefix to restrict results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "location": "string",
      "metageneration": "string",
      "name": "Ava Chen",
      "selfLink": "https://example.com",
      "storageClass": "string",
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
| `id` | string | Bucket resource ID. |
| `location` | string | Bucket location. |
| `metageneration` | string | Bucket metadata generation. |
| `name` | string | Bucket name. |
| `selfLink` | string | API URL for the bucket. |
| `storageClass` | string | Default storage class. |
| `timeCreated` | date | Bucket creation timestamp. |
| `updated` | date | Bucket update timestamp. |

## Native endpoint

Through the native Google Cloud Storage API, this operation is `GET /storage/v1/b` (base URL `https://storage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-buckets.md) for the provider-specific parameters and requirements.

