# CDR Platform: Purchase CO2 Removal

Creates a CO2 removal purchase in CDR Platform.

```
POST https://connect.mindcloud.co/v1/universal/cDRPlatform/latest/actions/purchase-co2-removal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CDR Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cDRPlatform/latest/actions/purchase-co2-removal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "weightUnit": "kg",
  "currency": "usd",
  "items[].methodType": "forestation",
  "items[].cdrAmount": "1000"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cDRPlatform/latest/actions/purchase-co2-removal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "weightUnit": "kg",
    "currency": "usd",
    "items[].methodType": "forestation",
    "items[].cdrAmount": "1000"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `weightUnit` | list<string> | yes | Unit for the CO2 removal amount. One of: `g`, `kg`, `t`. Example: `kg`. |
| `currency` | list<string> | yes | Currency for the purchase request. One of: `chf`, `eur`, `gbp`, `usd`. Example: `usd`. |
| `items[].methodType` | list<string> | yes | Carbon removal method type for an item. One of: `bio-oil`, `forestation`, `kelp-sinking`, `olivine`. Example: `forestation`. |
| `items[].cdrAmount` | number | yes | Amount of CO2 removal for an item, in the selected weight unit. Example: `1000`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientReferenceId` | string | no | Optional client reference ID to store with the purchase request. Example: `order-123`. |
| `certificateDisplayName` | string | no | Optional display name for the removal certificate. Example: `Earth Day removal`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "transaction_uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `transaction_uuid` | string | Unique transaction UUID for the CDR purchase request. |

## Native endpoint

Through the native CDR Platform API, this operation is `POST /v1/cdr/` (base URL `https://api.cdrplatform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/purchase-co2-removal.md) for the provider-specific parameters and requirements.

