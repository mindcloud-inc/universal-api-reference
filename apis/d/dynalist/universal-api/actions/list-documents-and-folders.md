# Dynalist: List Documents And Folders

Retrieves documents and folders from Dynalist.

```
GET https://connect.mindcloud.co/v1/universal/dynalist/latest/actions/list-documents-and-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dynalist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dynalist/latest/actions/list-documents-and-folders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dynalist/latest/actions/list-documents-and-folders?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "_code": "string",
      "_msg": "string",
      "files": [
        {}
      ],
      "root_file_id": "string"
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
| `files` | array<object> |  |
| `root_file_id` | string |  |

## Native endpoint

Through the native Dynalist API, this operation is `POST /file/list` (base URL `https://dynalist.io/api/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-documents-and-folders.md) for the provider-specific parameters and requirements.

