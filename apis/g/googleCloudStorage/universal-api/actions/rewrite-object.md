# Google Cloud Storage: Rewrite Object

Rewrites an object to a destination in Google Cloud Storage.

```
PUT https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/rewrite-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Storage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/rewrite-object" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/rewrite-object', {
  method: 'PUT',
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
| `destinationBucket` | list<string> | yes | Bucket to rewrite the object into. |
| `destinationObject` | string | yes | Destination object name. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `rewriteToken` | string | no | Token returned by a prior rewrite call when the rewrite is incomplete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "done": true,
      "kind": "string",
      "objectSize": "string",
      "resource": {},
      "rewriteToken": "string",
      "totalBytesRewritten": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `done` | boolean |  |
| `kind` | string |  |
| `objectSize` | string |  |
| `resource` | object |  |
| `rewriteToken` | string |  |
| `totalBytesRewritten` | string |  |

## Native endpoint

Through the native Google Cloud Storage API, this operation is `POST /storage/v1/b/:sourceBucket/o/:sourceObject/rewriteTo/b/:destinationBucket/o/:destinationObject` (base URL `https://storage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rewrite-object.md) for the provider-specific parameters and requirements.

