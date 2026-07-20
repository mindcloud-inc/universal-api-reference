# Uploadcare: Get Document Conversion Info

Retrieves document conversion info from Uploadcare.

```
GET https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/get-document-conversion-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uploadcare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/get-document-conversion-info?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/get-document-conversion-info?${params}`, {
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
| `uuid` | string | yes | Uploadcare file UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": {},
      "format": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | object | Conversion error details when present. |
| `format` | object | Detected source format and available conversion formats. |

## Native endpoint

Through the native Uploadcare API, this operation is `GET /convert/document/:uuid/` (base URL `https://api.uploadcare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-conversion-info.md) for the provider-specific parameters and requirements.

