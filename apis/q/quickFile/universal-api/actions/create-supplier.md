# QuickFile: Create Supplier



```
POST https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/create-supplier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/create-supplier" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/create-supplier', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyName` | string | yes | Supplier company or trading name to create. |
| `supplierReference` | string | no | Optional external reference or short account code for the supplier. |
| `city` | string | no | Town or city for the supplier address. |
| `addressLine1` | string | no | First postal address line. |
| `postcode` | string | no | Postal or ZIP code. |
| `countryIso` | string | no | Two-letter ISO country code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "supplierId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `supplierId` | number | QuickFile SupplierID created by the request. |

## Native endpoint

Through the native QuickFile API, this operation is `POST /supplier/create` (base URL `https://api.quickfile.co.uk/1_2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-supplier.md) for the provider-specific parameters and requirements.

