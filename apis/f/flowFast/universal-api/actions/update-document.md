# FlowFast: Update Document

Updates an existing document in FlowFast.

```
PUT https://connect.mindcloud.co/v1/universal/flowFast/latest/actions/update-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FlowFast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/flowFast/latest/actions/update-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flowFast/latest/actions/update-document', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | string | no |  |
| `title` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "id": "string",
      "title": "string",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `id` | string |  |
| `title` | string |  |
| `uid` | string |  |

## Native endpoint

Through the native FlowFast API, this operation is `PATCH /documents/:documentId` (base URL `https://apps.flowfast.io/api/latest/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-document.md) for the provider-specific parameters and requirements.

