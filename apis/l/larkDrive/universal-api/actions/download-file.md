# Lark Drive: Download File



```
GET https://connect.mindcloud.co/v1/universal/larkDrive/latest/actions/download-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lark Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/larkDrive/latest/actions/download-file?connectionId=$CONNECTION_ID&fileToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/larkDrive/latest/actions/download-file?${params}`, {
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
| `fileToken` | string | yes |  |

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

Through the native Lark Drive API, this operation is `GET /drive/v1/files/:file_token/download` (base URL `https://open.larksuite.com/open-apis`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-file.md) for the provider-specific parameters and requirements.

