# BigML: Create Model

Creates a model in BigML.

```
POST https://connect.mindcloud.co/v1/universal/bigML/latest/actions/create-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigML `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bigML/latest/actions/create-model" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "datasetId": "dataset/69cd1234abcd1234abcd1234"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bigML/latest/actions/create-model', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "datasetId": "dataset/69cd1234abcd1234abcd1234"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `datasetId` | string | yes | BigML dataset resource ID in full resource format (for example, dataset/69cd1234abcd1234abcd1234). Example: `dataset/69cd1234abcd1234abcd1234`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `objectiveField` | string | no | Optional dataset field identifier to predict. If omitted, BigML chooses the objective field automatically. Example: `000001`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "created": "string",
      "name": "Ava Chen",
      "resource": "string",
      "status": {},
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | HTTP-like response code from BigML. |
| `created` | string | Creation timestamp. |
| `name` | string | Created model name. |
| `resource` | string | Created model resource identifier. |
| `status` | object | BigML processing status object. |
| `updated` | string | Last update timestamp. |

## Native endpoint

Through the native BigML API, this operation is `POST /model` (base URL `https://bigml.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-model.md) for the provider-specific parameters and requirements.

