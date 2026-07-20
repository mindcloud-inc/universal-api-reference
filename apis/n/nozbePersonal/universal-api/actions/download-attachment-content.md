# Nozbe Personal: Download Attachment Content

Retrieves attachment file content from Nozbe Personal.

```
GET https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/download-attachment-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nozbe Personal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/download-attachment-content?connectionId=$CONNECTION_ID&commentId=string&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "commentId": "string",
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/download-attachment-content?${params}`, {
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
| `commentId` | string | yes | Comment ID from Nozbe. |
| `fileId` | string | yes | Attachment file ID from Nozbe. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Nozbe Personal API, this operation is `GET /comments/:comment_id/attachments/:file_id/content` (base URL `https://api4.nozbe.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-attachment-content.md) for the provider-specific parameters and requirements.

