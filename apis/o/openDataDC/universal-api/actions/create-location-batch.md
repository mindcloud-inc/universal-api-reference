# Open Data DC: Create Location Batch



```
POST https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/create-location-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Data DC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/create-location-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "address_base64": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/create-location-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "address_base64": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address_base64` | string | yes | Base64 encoded addresses in JSON object. |

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

Through the native Open Data DC API, this operation is `POST /api/v2.2/locationbatch` (base URL `https://datagate.dc.gov/mar/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-location-batch.md) for the provider-specific parameters and requirements.

