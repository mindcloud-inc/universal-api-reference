# QuickFile: Update Supplier



```
PUT https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/update-supplier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/update-supplier" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "supplierId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/update-supplier', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "supplierId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `supplierId` | number | yes | QuickFile SupplierID to update. |
| `companyName` | string | no | Updated supplier company or trading name. |
| `supplierReference` | string | no | Updated external reference or short account code. |
| `city` | string | no | Updated town or city. |
| `addressLine1` | string | no | Updated first postal address line. |
| `postcode` | string | no | Updated postal or ZIP code. |
| `countryIso` | string | no | Updated two-letter ISO country code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "supplierDetailsUpdated": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `supplierDetailsUpdated` | boolean | Whether the supplier details payload was applied. |

## Native endpoint

Through the native QuickFile API, this operation is `POST /supplier/update` (base URL `https://api.quickfile.co.uk/1_2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-supplier.md) for the provider-specific parameters and requirements.

