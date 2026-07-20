# Uploadcare: Get Document Conversion Status

Retrieves document conversion status from Uploadcare by token.

```
GET https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/get-document-conversion-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uploadcare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/get-document-conversion-status?connectionId=$CONNECTION_ID&token=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "token": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/get-document-conversion-status?${params}`, {
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
| `token` | number | yes | Conversion job token. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": {},
      "result": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | object | Conversion error details when present. |
| `result` | object | Conversion result details, including the converted file UUID. |
| `status` | string | Current conversion status. |

## Native endpoint

Through the native Uploadcare API, this operation is `GET /convert/document/status/:token/` (base URL `https://api.uploadcare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-conversion-status.md) for the provider-specific parameters and requirements.

