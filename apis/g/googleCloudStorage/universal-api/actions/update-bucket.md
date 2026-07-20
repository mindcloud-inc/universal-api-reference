# Google Cloud Storage: Update Bucket

Updates an existing bucket in Google Cloud Storage.

```
PUT https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/update-bucket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Storage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/update-bucket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bucket": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/update-bucket', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bucket": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bucket` | list<string> | yes | Bucket name. |
| `labels` | object | no | Bucket labels object to patch. |
| `storageClass` | list<string> | no | Default storage class to patch. One of: `ARCHIVE`, `COLDLINE`, `NEARLINE`, `RAPID`, `STANDARD`. |

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

Through the native Google Cloud Storage API, this operation is `PATCH /storage/v1/b/:bucket` (base URL `https://storage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-bucket.md) for the provider-specific parameters and requirements.

