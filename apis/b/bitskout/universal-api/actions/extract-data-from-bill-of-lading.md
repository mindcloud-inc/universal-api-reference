# Bitskout: Extract Data from Bill of Lading

Extracts bill of lading data with a Bitskout plugin.

```
POST https://connect.mindcloud.co/v1/universal/bitskout/latest/actions/extract-data-from-bill-of-lading
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitskout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bitskout/latest/actions/extract-data-from-bill-of-lading" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bitskout/latest/actions/extract-data-from-bill-of-lading', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileUrl` | string | no | Direct download URL for the bill of lading file to extract. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "outputs": {
        "BL Number": "string",
        "BOL Type": "string",
        "Booking N": "string",
        "Consignee": "string",
        "Notify Party": "string",
        "Port of Discharge": "string",
        "Port of Loading": "string",
        "RawJSON": "string",
        "ShippedOnBoard": "string",
        "Shipper": "string",
        "Vessel": "string",
        "VoyageN": "string",
        "Weight": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `outputs` | object | Bill of lading extraction outputs |
| `outputs.BL Number` | string | Bill of Lading Number |
| `outputs.BOL Type` | string | Bill of Lading Type |
| `outputs.Booking N` | string | Booking Number |
| `outputs.Consignee` | string | Consignee |
| `outputs.Notify Party` | string | Notify Party |
| `outputs.Port of Discharge` | string | Port of Discharge |
| `outputs.Port of Loading` | string | Port of Loading |
| `outputs.RawJSON` | string | Raw JSON |
| `outputs.ShippedOnBoard` | string | Shipped on Board |
| `outputs.Shipper` | string | Shipper |
| `outputs.Vessel` | string | Vessel |
| `outputs.VoyageN` | string | Voyage Number |
| `outputs.Weight` | string | Weight |

## Native endpoint

Through the native Bitskout API, this operation is `POST /actions/bill_of_lading` (base URL `https://api.bitskout.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-data-from-bill-of-lading.md) for the provider-specific parameters and requirements.

