# DateX (Legacy): List Inventory



```
GET https://connect.mindcloud.co/v1/universal/dateX/latest/actions/list-inventory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DateX (Legacy) `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dateX/latest/actions/list-inventory?connectionId=$CONNECTION_ID&limit=25&offset=0&warehouse=string&filters.project=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "warehouse": "string",
  "filters.project": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dateX/latest/actions/list-inventory?${params}`, {
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
| `filters.owner` | string | no |  |
| `warehouse` | string | yes |  |
| `filters` | object<object> | no |  |
| `filters.project` | string | yes |  |
| `filters.material` | string | no |  |
| `outputWeightUOM` | string | no |  |
| `filters.lot` | string | no |  |
| `filters.vendorLot` | string | no |  |
| `filters.upc` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isFixedWeight": true,
      "licensePlate": "string",
      "lot": "string",
      "material": "string",
      "owner": "string",
      "packagedAmount": 1,
      "packaging": "string",
      "packagingGrossWeight": 1,
      "packagingNetWeight": 1,
      "project": "string",
      "serialNumbers": {},
      "totalGrossWeight": 1,
      "totalNetWeight": 1,
      "upc": {},
      "vendorLot": "string",
      "weightUom": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isFixedWeight` | boolean |  |
| `licensePlate` | string |  |
| `lot` | string |  |
| `material` | string |  |
| `owner` | string |  |
| `packagedAmount` | number |  |
| `packaging` | string |  |
| `packagingGrossWeight` | number |  |
| `packagingNetWeight` | number |  |
| `project` | string |  |
| `serialNumbers` | object |  |
| `totalGrossWeight` | number |  |
| `totalNetWeight` | number |  |
| `upc` | object |  |
| `vendorLot` | string |  |
| `weightUom` | string |  |

## Native endpoint

Through the native DateX (Legacy) API, this operation is `POST inventory/get` (base URL `https://{{credentials.environment}}.wavelength.host/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-inventory.md) for the provider-specific parameters and requirements.

