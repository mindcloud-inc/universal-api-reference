# BigML: Create Dataset

Creates a dataset in BigML.

```
POST https://connect.mindcloud.co/v1/universal/bigML/latest/actions/create-dataset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigML `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bigML/latest/actions/create-dataset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceId": "source/69cd1234abcd1234abcd1234"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bigML/latest/actions/create-dataset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceId": "source/69cd1234abcd1234abcd1234"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceId` | string | yes | BigML source resource ID in full resource format (for example, source/69cd1234abcd1234abcd1234). Example: `source/69cd1234abcd1234abcd1234`. |

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
| `name` | string | Created dataset name. |
| `resource` | string | Created dataset resource identifier. |
| `status` | object | BigML processing status object. |
| `updated` | string | Last update timestamp. |

## Native endpoint

Through the native BigML API, this operation is `POST /dataset` (base URL `https://bigml.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-dataset.md) for the provider-specific parameters and requirements.

