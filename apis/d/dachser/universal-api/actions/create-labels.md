# Dachser: Create Labels

Creates shipping labels for a shipment in Dachser.

```
POST https://connect.mindcloud.co/v1/universal/dachser/latest/actions/create-labels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dachser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dachser/latest/actions/create-labels" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "shipment": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dachser/latest/actions/create-labels', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "shipment": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `format` | string | no | Label format. Use P for PDF or Z for ZPL. Default: `P`. |
| `count` | number | no | Number of labels to receive. Maximum 10. Default: `1`. |
| `shipment` | object | yes | Shipment data to render labels for. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fontFileName` | string | no | Font file name for ZPL label format. Default: `ARIALR.FNT`. |
| `acceptLanguage` | string | no | Optional language sent as the Accept-Language header. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "label": [
        "string"
      ],
      "relation": {},
      "ssccs": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `label` | array<string> |  |
| `relation` | object |  |
| `ssccs` | array<string> |  |

## Native endpoint

Through the native Dachser API, this operation is `POST /rest/v2/labels` (base URL `https://api-gateway.dachser.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-labels.md) for the provider-specific parameters and requirements.

