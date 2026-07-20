# Convertio: Get Result File Content

Retrieves converted file content from Convertio.

```
GET https://connect.mindcloud.co/v1/universal/convertio/latest/actions/get-result-file-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Convertio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/convertio/latest/actions/get-result-file-content?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/convertio/latest/actions/get-result-file-content?${params}`, {
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
| `id` | string | yes | Conversion ID returned by Start Conversion. |
| `type` | string | no | Response encoding type. Convertio documents `base64`. Default: `base64`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data` | object |  |
| `status` | string |  |

## Native endpoint

Through the native Convertio API, this operation is `GET /convert/:id/dl/:type` (base URL `https://api.convertio.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-result-file-content.md) for the provider-specific parameters and requirements.

