# Lark Drive: Get File Statistics



```
GET https://connect.mindcloud.co/v1/universal/larkDrive/latest/actions/get-file-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lark Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/larkDrive/latest/actions/get-file-statistics?connectionId=$CONNECTION_ID&fileToken=string&fileType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileToken": "string",
  "fileType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/larkDrive/latest/actions/get-file-statistics?${params}`, {
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
| `fileType` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {
        "file_token": "string",
        "file_type": "string",
        "statistics": {
          "like_count": 1,
          "pv": 1,
          "timestamp": 1,
          "uv": 1
        }
      },
      "msg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data.file_token` | string |  |
| `data.file_type` | string |  |
| `data.statistics.like_count` | number |  |
| `data.statistics.pv` | number |  |
| `data.statistics.timestamp` | number |  |
| `data.statistics.uv` | number |  |
| `msg` | string |  |

## Native endpoint

Through the native Lark Drive API, this operation is `GET /drive/v1/files/:file_token/statistics` (base URL `https://open.larksuite.com/open-apis`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file-statistics.md) for the provider-specific parameters and requirements.

