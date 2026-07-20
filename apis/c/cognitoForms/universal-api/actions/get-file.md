# Cognito Forms: Get File



```
GET https://connect.mindcloud.co/v1/universal/cognitoForms/latest/actions/get-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cognito Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cognitoForms/latest/actions/get-file?connectionId=$CONNECTION_ID&formId=string&entryId=string&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string",
  "entryId": "string",
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cognitoForms/latest/actions/get-file?${params}`, {
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
| `formId` | string | yes |  |
| `entryId` | string | yes |  |
| `fileId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "contentType": "string",
      "file": "string",
      "id": "string",
      "name": "Ava Chen",
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Base64-encoded file content. |
| `contentType` | string | MIME type for the file. |
| `file` | string | Download URL for the file. |
| `id` | string | File ID. |
| `name` | string | File name. |
| `size` | number | File size in bytes. |

## Native endpoint

Through the native Cognito Forms API, this operation is `GET /forms/:formId/entries/:entryId/files/:fileId` (base URL `https://www.cognitoforms.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file.md) for the provider-specific parameters and requirements.

