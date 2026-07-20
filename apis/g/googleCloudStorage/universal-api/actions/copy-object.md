# Google Cloud Storage: Copy Object

Copies an object to a destination in Google Cloud Storage.

```
POST https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/copy-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Storage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/copy-object" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceBucket": "string",
  "sourceObject": "string",
  "destinationBucket": "string",
  "destinationObject": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/copy-object', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceBucket": "string",
    "sourceObject": "string",
    "destinationBucket": "string",
    "destinationObject": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceBucket` | list<string> | yes | Bucket containing the source object. |
| `sourceObject` | string | yes | Source object name. |
| `destinationBucket` | list<string> | yes | Bucket to copy the object into. |
| `destinationObject` | string | yes | Destination object name. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `metadata` | object | no | Optional replacement custom metadata. |

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
| `name` | string |  |
| `size` | string |  |
| `timeCreated` | date |  |
| `updated` | date |  |

## Native endpoint

Through the native Google Cloud Storage API, this operation is `POST /storage/v1/b/:sourceBucket/o/:sourceObject/copyTo/b/:destinationBucket/o/:destinationObject` (base URL `https://storage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/copy-object.md) for the provider-specific parameters and requirements.

