# Kintone: Download File

Downloads a file from Kintone.

```
GET https://connect.mindcloud.co/v1/universal/kintone/latest/actions/download-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kintone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kintone/latest/actions/download-file?connectionId=$CONNECTION_ID&fileKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kintone/latest/actions/download-file?${params}`, {
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
| `fileKey` | string | yes | The Kintone file key returned by an upload or file field. |

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
| `data` | array<number> | Binary file bytes returned by the Kintone download response. |
| `type` | string | Node-style buffer marker returned by the raw-response pipeline. |

## Native endpoint

Through the native Kintone API, this operation is `GET /file.json` (base URL `{{credentials.baseUrl}}/k/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-file.md) for the provider-specific parameters and requirements.

