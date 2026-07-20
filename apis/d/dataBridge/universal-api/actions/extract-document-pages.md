# DataBridge: Extract Document Pages

Extracts pages from a document in DataBridge.

```
POST https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/extract-document-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataBridge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/extract-document-pages" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/extract-document-pages', {
  method: 'POST',
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "documentId": "string",
      "endPage": 1,
      "pages": [
        "string"
      ],
      "startPage": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentId` | string |  |
| `endPage` | number |  |
| `pages` | array<string> |  |
| `startPage` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native DataBridge API, this operation is `POST /documents/pages` (base URL `https://api.morphik.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-document-pages.md) for the provider-specific parameters and requirements.

