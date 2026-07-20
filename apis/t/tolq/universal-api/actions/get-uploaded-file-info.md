# Tolq: Get Uploaded File Info

Retrieves uploaded file details from Tolq.

```
GET https://connect.mindcloud.co/v1/universal/tolq/latest/actions/get-uploaded-file-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tolq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tolq/latest/actions/get-uploaded-file-info?connectionId=$CONNECTION_ID&uid=a8d75d4706f38108d0dd86f7" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "a8d75d4706f38108d0dd86f7"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tolq/latest/actions/get-uploaded-file-info?${params}`, {
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
| `uid` | string | yes | Uploaded file UID returned by Initiate File Upload. Example: `a8d75d4706f38108d0dd86f7`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "fileName": "Ava Chen",
      "hasRowsAndColumns": true,
      "id": 1,
      "keys": {},
      "processing": true,
      "sourceLanguageCode": "string",
      "status": "string",
      "supportsPlainText": true,
      "totalColumns": 1,
      "totalRows": 1,
      "uid": "string",
      "wordCount": 1,
      "xliffBased": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string |  |
| `fileName` | string |  |
| `hasRowsAndColumns` | boolean |  |
| `id` | number |  |
| `keys` | object |  |
| `processing` | boolean |  |
| `sourceLanguageCode` | string |  |
| `status` | string |  |
| `supportsPlainText` | boolean |  |
| `totalColumns` | number |  |
| `totalRows` | number |  |
| `uid` | string |  |
| `wordCount` | number |  |
| `xliffBased` | boolean |  |

## Native endpoint

Through the native Tolq API, this operation is `GET /translations/requests/files/:uid` (base URL `https://api.tolq.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-uploaded-file-info.md) for the provider-specific parameters and requirements.

