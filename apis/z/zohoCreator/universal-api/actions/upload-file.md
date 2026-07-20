# Zoho Creator: Upload File

Uploads a file to a Zoho Creator record.

```
POST https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/upload-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Creator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/upload-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountOwnerName": "Ava Chen",
  "appLinkName": "https://example.com",
  "fieldLinkName": "https://example.com",
  "file": "string",
  "recordId": "string",
  "reportLinkName": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCreator/latest/actions/upload-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountOwnerName": "Ava Chen",
    "appLinkName": "https://example.com",
    "fieldLinkName": "https://example.com",
    "file": "string",
    "recordId": "string",
    "reportLinkName": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountOwnerName` | string | yes | Zoho Creator account owner name. |
| `appLinkName` | string | yes | Zoho Creator app link name. |
| `fieldLinkName` | string | yes | Zoho Creator field link name for the file field. |
| `file` | file | yes | Binary file content to upload into the file field. |
| `recordId` | string | yes | Zoho Creator record ID. |
| `reportLinkName` | string | yes | Zoho Creator report link name. |
| `skipWorkflow[]` | array<string> | no | Workflows to skip during the upload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Zoho Creator response code. |
| `data` | object | Uploaded file metadata returned by Zoho Creator. |

## Native endpoint

Through the native Zoho Creator API, this operation is `POST /data/:account_owner_name/:app_link_name/report/:report_link_name/:record_ID/:field_link_name/upload` (base URL `https://www.zohoapis.com/creator/v2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file.md) for the provider-specific parameters and requirements.

