# Convertio: Start Conversion

Starts a conversion in Convertio.

```
POST https://connect.mindcloud.co/v1/universal/convertio/latest/actions/start-conversion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Convertio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/convertio/latest/actions/start-conversion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "outputFormat": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/convertio/latest/actions/start-conversion', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "outputFormat": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | string | no | URL of the input file when input=url, or file content when input=raw/base64. Omit for input=upload. |
| `filename` | string | no | Input filename including extension. Required when input=raw/base64. |
| `input` | string | no | How the input file is provided. Default: `url`. |
| `outputFormat` | string | yes | Target file format for the conversion result. |

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

Through the native Convertio API, this operation is `POST /convert` (base URL `https://api.convertio.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-conversion.md) for the provider-specific parameters and requirements.

