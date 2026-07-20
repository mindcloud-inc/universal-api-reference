# Google Docs: List Documents

Finds Google Docs and Word documents in Google Drive.

```
GET https://connect.mindcloud.co/v1/universal/googleDocs/latest/actions/list-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Docs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleDocs/latest/actions/list-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleDocs/latest/actions/list-documents?${params}`, {
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
| `folderId` | list<string> | no | Id of the folder |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "mimeType": "string",
      "name": "Ava Chen",
      "parents": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `mimeType` | string |  |
| `name` | string |  |
| `parents` | array |  |

## Native endpoint

Through the native Google Docs API, this operation is `GET https://www.googleapis.com/drive/v3/files` (base URL `https://docs.googleapis.com/v1/documents`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-documents.md) for the provider-specific parameters and requirements.

