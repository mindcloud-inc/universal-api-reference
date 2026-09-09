# Acumatica: Release Payment



```
PUT https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/release-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/release-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entity.Type.value": "Payment",
  "entity.ReferenceNbr.value": "000123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/release-payment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entity.Type.value": "Payment",
    "entity.ReferenceNbr.value": "000123"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entity` | object | no |  |
| `entity.Type` | object | no |  |
| `entity.Type.value` | string | yes | Example: `Payment`. |
| `entity.ReferenceNbr` | object | no |  |
| `entity.ReferenceNbr.value` | string | yes | Example: `000123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Acumatica API, this operation is `POST /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Payment/ReleasePayment` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/release-payment.md) for the provider-specific parameters and requirements.

