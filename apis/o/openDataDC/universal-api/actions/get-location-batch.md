# Open Data DC: Get Location Batch



```
GET https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/get-location-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Data DC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/get-location-batch?connectionId=$CONNECTION_ID&address_base64=string&address_separator=%7C%7C&chunkSequnce_separator=%3A&parallel=false" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address_base64": "string",
  "address_separator": "||",
  "chunkSequnce_separator": ":",
  "parallel": "false"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/get-location-batch?${params}`, {
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
| `address_base64` | string | yes | Base64 encoded address string. |
| `address_separator` | string | yes | Address separator, default \|\|. Default: `\|\|`. |
| `chunkSequnce_separator` | string | yes | Chunk sequence separator, default colon. Default: `:`. |
| `parallel` | boolean | yes | Whether to use parallel processing. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Message": "string",
      "Result": {
        "addresses": [
          {}
        ]
      },
      "Success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Message` | string | Provider message. |
| `Result` | object | Location result payload. |
| `Result.addresses` | array<object> | Matched address records. |
| `Success` | boolean | Whether the request succeeded. |

## Native endpoint

Through the native Open Data DC API, this operation is `GET /api/v2.2/locationbatch/:address_base64/:address_separator/:chunkSequnce_separator/:parallel` (base URL `https://datagate.dc.gov/mar/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-location-batch.md) for the provider-specific parameters and requirements.

