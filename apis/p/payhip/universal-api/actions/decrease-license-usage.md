# Payhip: Decrease License Usage

Decreases a Payhip license key usage count.

```
PUT https://connect.mindcloud.co/v1/universal/payhip/latest/actions/decrease-license-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Payhip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/payhip/latest/actions/decrease-license-usage" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "licenseKey": "PH-ABCD-1234-EFGH"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payhip/latest/actions/decrease-license-usage', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "licenseKey": "PH-ABCD-1234-EFGH"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `licenseKey` | string | yes | The Payhip license key whose usage count should be decreased. Example: `PH-ABCD-1234-EFGH`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "buyerEmail": "ava@example.com",
      "date": "string",
      "enabled": true,
      "licenseKey": "string",
      "productLink": "https://example.com",
      "productName": "Ava Chen",
      "uses": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `buyerEmail` | string | The buyer email associated with the license key. |
| `date` | string | The Payhip timestamp returned for the license record. |
| `enabled` | boolean | Whether the license key is enabled. |
| `licenseKey` | string | The Payhip license key. |
| `productLink` | string | The Payhip product URL associated with the license key. |
| `productName` | string | The Payhip product name associated with the license key. |
| `uses` | number | The current usage count for the license key. |

## Native endpoint

Through the native Payhip API, this operation is `PUT /license/decrease` (base URL `https://payhip.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/decrease-license-usage.md) for the provider-specific parameters and requirements.

