# IgniSign: Upload Document Content Data JSON



```
PUT https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/upload-document-content-data-json
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IgniSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/upload-document-content-data-json" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/upload-document-content-data-json', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | string | yes | The IgniSign document ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "dataVisualizationAvailable": true,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `dataVisualizationAvailable` | boolean |  |
| `status` | string |  |

## Native endpoint

Through the native IgniSign API, this operation is `POST /v4/documents/:documentId/data-json-content` (base URL `https://api.ignisign.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-document-content-data-json.md) for the provider-specific parameters and requirements.

