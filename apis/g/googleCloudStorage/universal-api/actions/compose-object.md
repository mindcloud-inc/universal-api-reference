# Google Cloud Storage: Compose Object

Composes multiple objects into one in Google Cloud Storage.

```
POST https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/compose-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Storage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/compose-object" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "destinationBucket": "string",
  "destinationObject": "string",
  "sourceObjects[]": [
    {}
  ],
  "sourceObjects[].name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleCloudStorage/latest/actions/compose-object', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "destinationBucket": "string",
    "destinationObject": "string",
    "sourceObjects[]": [{}],
    "sourceObjects[].name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `destinationBucket` | list<string> | yes | Bucket to create the composed object in. |
| `destinationObject` | string | yes | Destination object name. |
| `sourceObjects[]` | array<object> | yes | Source object entries to compose. |
| `sourceObjects[].name` | string | yes | Name of a source object to compose. All source objects must be in the selected destination bucket. |
| `sourceObjects[].generation` | string | no | Generation of the source object to use. |
| `sourceObjects[].objectPreconditions` | object | no | Conditions that must be met for the source object to be used in composition. |
| `sourceObjects[].objectPreconditions.ifGenerationMatch` | string | no | Only compose if the source object generation matches this value. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deleteSourceObjects` | boolean | no | Whether to delete source objects after composition. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bucket": "string",
      "componentCount": 1,
      "contentType": "string",
      "generation": "string",
      "id": "string",
      "name": "Ava Chen",
      "size": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bucket` | string |  |
| `componentCount` | number |  |
| `contentType` | string |  |
| `generation` | string |  |
| `id` | string |  |
| `name` | string |  |
| `size` | string |  |

## Native endpoint

Through the native Google Cloud Storage API, this operation is `POST /storage/v1/b/:destinationBucket/o/:destinationObject/compose` (base URL `https://storage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/compose-object.md) for the provider-specific parameters and requirements.

