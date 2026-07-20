# 2Smart Cloud: Update build part



```
PUT https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/factory-vendor-build-parts-by-id-factory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/factory-vendor-build-parts-by-id-factory" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/factory-vendor-build-parts-by-id-factory', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | ID of entity |
| `is_factory` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "binary_url": "https://example.com",
      "created": "string",
      "id": 1,
      "is_factory": true,
      "offset": 1,
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `binary_url` | string |  |
| `created` | string |  |
| `id` | number |  |
| `is_factory` | boolean |  |
| `offset` | number |  |
| `updated` | string |  |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `POST /vendor/build-parts/{id}/factory` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/factory-vendor-build-parts-by-id-factory.md) for the provider-specific parameters and requirements.

