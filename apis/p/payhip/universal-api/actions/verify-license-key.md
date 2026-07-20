# Payhip: Verify License Key

Verifies a Payhip license key and returns its details.

```
GET https://connect.mindcloud.co/v1/universal/payhip/latest/actions/verify-license-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Payhip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payhip/latest/actions/verify-license-key?connectionId=$CONNECTION_ID&licenseKey=PH-ABCD-1234-EFGH" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "licenseKey": "PH-ABCD-1234-EFGH"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payhip/latest/actions/verify-license-key?${params}`, {
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
| `licenseKey` | string | yes | The Payhip license key to verify. Example: `PH-ABCD-1234-EFGH`. |

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

Through the native Payhip API, this operation is `GET /license/verify` (base URL `https://payhip.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-license-key.md) for the provider-specific parameters and requirements.

