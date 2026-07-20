# Convertio: Upload Conversion File

Uploads a file for a conversion in Convertio.

```
PUT https://connect.mindcloud.co/v1/universal/convertio/latest/actions/upload-conversion-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Convertio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/convertio/latest/actions/upload-conversion-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "filename": "Ava Chen",
  "id": "string",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/convertio/latest/actions/upload-conversion-file', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "filename": "Ava Chen",
    "id": "string",
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filename` | string | yes | Input filename including extension. |
| `id` | string | yes | Conversion ID returned by Start Conversion. |
| `file` | file | yes | Binary file contents to upload for the conversion. |

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

Through the native Convertio API, this operation is `PUT /convert/:id/:filename` (base URL `https://api.convertio.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-conversion-file.md) for the provider-specific parameters and requirements.

