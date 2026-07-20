# SigningHub: Change Document Order

Updates document order in SigningHub.

```
PUT https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/change-document-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigningHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/change-document-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "packageId": "11191608",
  "documentId": "13459159",
  "order": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/change-document-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "packageId": "11191608",
    "documentId": "13459159",
    "order": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `packageId` | number | yes | The document package containing the document to reorder. Example: `11191608`. |
| `documentId` | number | yes | The document to reorder. Example: `13459159`. |
| `order` | number | yes | The new document order position. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "package_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `package_name` | string |  |

## Native endpoint

Through the native SigningHub API, this operation is `PUT /v4/packages/:packageId/documents/:documentId/reorder` (base URL `https://api.signinghub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-document-order.md) for the provider-specific parameters and requirements.

