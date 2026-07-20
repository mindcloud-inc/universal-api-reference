# AnyDB: Complete Upload

Completes an attachment upload in AnyDB.

```
PUT https://connect.mindcloud.co/v1/universal/anyDB/latest/actions/complete-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AnyDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/anyDB/latest/actions/complete-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileSize": 1,
  "teamId": "string",
  "databaseId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anyDB/latest/actions/complete-upload', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileSize": 1,
    "teamId": "string",
    "databaseId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileSize` | number | yes | The uploaded file size in bytes. |
| `teamId` | string | yes | The AnyDB team ID. |
| `databaseId` | string | yes | The AnyDB database ID. |
| `recordId` | string | no | Optional AnyDB record ID for the upload target. |
| `cellPosition` | string | no | Optional AnyDB cell position for the completed upload. |
| `importContent` | boolean | no | Whether the completed upload should import content. |
| `importAttachTo` | string | no | Optional AnyDB parent ID to attach the imported upload to. |
| `importTemplateId` | string | no | Optional AnyDB template ID for the imported upload. |
| `importFilename` | string | no | Optional final filename for the completed upload. |
| `importImage` | boolean | no | Whether the completed upload should be treated as an image. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AnyDB API returns.

## Native endpoint

Through the native AnyDB API, this operation is `PUT /api/integrations/ext/completeupload` (base URL `https://app.anydb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/complete-upload.md) for the provider-specific parameters and requirements.

