# FlowiseAI: Upsert Document Store

Upserts documents in a FlowiseAI document store.

```
PUT https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/upsert-document-store
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FlowiseAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/upsert-document-store" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flowiseAI/latest/actions/upsert-document-store', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | no | JSON body with documented document store upsert fields. |
| `id` | string | yes | Document store ID for upsert. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addedDocs": [
        {}
      ],
      "numAdded": 1,
      "numDeleted": 1,
      "numSkipped": 1,
      "numUpdated": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedDocs` | array<object> |  |
| `numAdded` | number |  |
| `numDeleted` | number |  |
| `numSkipped` | number |  |
| `numUpdated` | number |  |

## Native endpoint

Through the native FlowiseAI API, this operation is `POST /document-store/upsert/{id}` (base URL `https://cloud.flowiseai.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-document-store.md) for the provider-specific parameters and requirements.

