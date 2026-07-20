# PDF Blocks: Remove Restrictions

Updates a PDF document by removing restrictions in PDF Blocks.

```
PUT https://connect.mindcloud.co/v1/universal/pDFBlocks/latest/actions/remove-restrictions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF Blocks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pDFBlocks/latest/actions/remove-restrictions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFBlocks/latest/actions/remove-restrictions', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | The input PDF document. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PDF Blocks API returns.

## Native endpoint

Through the native PDF Blocks API, this operation is `POST /v1/remove_restrictions` (base URL `https://api.pdfblocks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-restrictions.md) for the provider-specific parameters and requirements.

