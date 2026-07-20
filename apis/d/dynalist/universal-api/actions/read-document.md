# Dynalist: Read Document

Retrieves a document from Dynalist.

```
GET https://connect.mindcloud.co/v1/universal/dynalist/latest/actions/read-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dynalist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dynalist/latest/actions/read-document?connectionId=$CONNECTION_ID&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dynalist/latest/actions/read-document?${params}`, {
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
| `fileId` | string | yes | ID of the document to read. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_code": "string",
      "_msg": "string",
      "file_id": "string",
      "nodes": [
        {}
      ],
      "title": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_code` | string |  |
| `_msg` | string |  |
| `file_id` | string |  |
| `nodes` | array<object> |  |
| `title` | string |  |
| `version` | number |  |

## Native endpoint

Through the native Dynalist API, this operation is `POST /doc/read` (base URL `https://dynalist.io/api/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/read-document.md) for the provider-specific parameters and requirements.

