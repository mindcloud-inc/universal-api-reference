# Google Cloud Storage: Get Bucket

Retrieves bucket metadata from Google Cloud Storage.

```
GET https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/get-bucket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Storage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/get-bucket?connectionId=$CONNECTION_ID&bucket=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bucket": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/get-bucket?${params}`, {
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
| `id` | string |  |
| `location` | string |  |
| `metageneration` | string |  |
| `name` | string |  |
| `selfLink` | string |  |
| `storageClass` | string |  |
| `timeCreated` | date |  |
| `updated` | date |  |

## Native endpoint

Through the native Google Cloud Storage API, this operation is `GET /storage/v1/b/:bucket` (base URL `https://storage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bucket.md) for the provider-specific parameters and requirements.

