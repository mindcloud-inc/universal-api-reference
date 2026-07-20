# Google Cloud Storage: Move Object

Moves an object within a bucket in Google Cloud Storage.

```
PUT https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/move-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Storage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/move-object" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bucket": "string",
  "sourceObject": "string",
  "destinationObject": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/move-object', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bucket": "string",
    "sourceObject": "string",
    "destinationObject": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bucket` | list<string> | yes | Bucket containing the object. |
| `sourceObject` | string | yes | Current object name. |
| `destinationObject` | string | yes | New object name. |

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
      "name": "Ava Chen",
      "size": "string",
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
| `name` | string |  |
| `size` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native Google Cloud Storage API, this operation is `POST /storage/v1/b/:bucket/o/:sourceObject/moveTo/o/:destinationObject` (base URL `https://storage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-object.md) for the provider-specific parameters and requirements.

