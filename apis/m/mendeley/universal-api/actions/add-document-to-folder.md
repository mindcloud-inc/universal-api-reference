# Mendeley: Add Document To Folder



```
POST https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/add-document-to-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendeley `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/add-document-to-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "folderId": "4e12ce22-eb4f-45f4-836c-37d13e7ec36d",
  "documentId": "ec9b2249-ab38-354b-8828-740d2a192353"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/add-document-to-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "folderId": "4e12ce22-eb4f-45f4-836c-37d13e7ec36d",
    "documentId": "ec9b2249-ab38-354b-8828-740d2a192353"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `folderId` | string | yes | Identifier of the folder. Example: `4e12ce22-eb4f-45f4-836c-37d13e7ec36d`. |
| `documentId` | string | yes | Identifier of the document to add to the folder. Example: `ec9b2249-ab38-354b-8828-740d2a192353`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Mendeley API returns.

## Native endpoint

Through the native Mendeley API, this operation is `POST /folders/:id/documents` (base URL `https://api.mendeley.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-document-to-folder.md) for the provider-specific parameters and requirements.

