# AnyDB: Get Upload URL

Retrieves a direct upload URL for AnyDB attachments.

```
GET https://connect.mindcloud.co/v1/universal/anyDB/latest/actions/get-upload-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AnyDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anyDB/latest/actions/get-upload-url?connectionId=$CONNECTION_ID&filename=Ava%20Chen&teamId=string&databaseId=string&recordId=string&fileSize=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filename": "Ava Chen",
  "teamId": "string",
  "databaseId": "string",
  "recordId": "string",
  "fileSize": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anyDB/latest/actions/get-upload-url?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filename` | string | yes | The filename to upload. |
| `teamId` | string | yes | The AnyDB team ID. |
| `databaseId` | string | yes | The AnyDB database ID. |
| `recordId` | string | yes | The AnyDB record ID. |
| `fileSize` | number | yes | The file size in bytes. |
| `cellPosition` | string | no | Optional AnyDB cell position to upload into. |
| `importContent` | boolean | no | Whether the uploaded asset should be imported as content. |
| `importMedia` | boolean | no | Whether the uploaded asset should be imported as media. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AnyDB API returns.

## Native endpoint

Through the native AnyDB API, this operation is `GET /api/integrations/ext/getuploadurl` (base URL `https://app.anydb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-upload-url.md) for the provider-specific parameters and requirements.

