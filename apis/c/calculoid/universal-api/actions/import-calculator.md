# Calculoid: Import Calculator



```
POST https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/import-calculator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calculoid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/import-calculator" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "calculator": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/import-calculator', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "calculator": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `calculator` | object | yes | Calculator import payload exported from Calculoid. Default: `{}`. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alerts": [
        {
          "msg": "string",
          "type": "string"
        }
      ],
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alerts[].msg` | string |  |
| `alerts[].type` | string |  |
| `id` | number |  |

## Native endpoint

Through the native Calculoid API, this operation is `POST /calculators/import` (base URL `https://api.calculoid.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-calculator.md) for the provider-specific parameters and requirements.

