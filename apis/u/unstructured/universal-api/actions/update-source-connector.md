# Unstructured: Update Source Connector

Updates a source connector in Unstructured.

```
PUT https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/update-source-connector
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unstructured `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/update-source-connector" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/update-source-connector', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceId` | string | yes | The source connector ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "config": {},
      "createdAt": "string",
      "id": "string",
      "name": "Ava Chen",
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `config` | object |  |
| `createdAt` | string |  |
| `id` | string |  |
| `name` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Unstructured API, this operation is `PUT /sources/:source_id` (base URL `https://platform.unstructuredapp.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-source-connector.md) for the provider-specific parameters and requirements.

