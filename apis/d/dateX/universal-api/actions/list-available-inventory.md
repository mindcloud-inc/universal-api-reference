# DateX (Legacy): List Available Inventory



```
GET https://connect.mindcloud.co/v1/universal/dateX/latest/actions/list-available-inventory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DateX (Legacy) `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dateX/latest/actions/list-available-inventory?connectionId=$CONNECTION_ID&limit=25&offset=0&warehouse=string&filters.project=string" \
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

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dateX/latest/actions/list-available-inventory?${params}`, {
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
| `paging.skip` | number | no | Default: `-1`. |
| `warehouse` | string | yes |  |
| `filters` | object<object> | no |  |
| `filters.project` | string | yes |  |
| `paging.top` | number | no | Default: `100`. |
| `filters.material` | string | no |  |
| `outputWeightUOM` | string | no |  |
| `filters.lot` | string | no |  |
| `paging` | object | no |  |
| `filters.vendorLot` | string | no |  |
| `filters.uPC` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availableBaseAmount": 1,
      "availablePackagedAmount": 1,
      "basePackaging": "string",
      "basePackagingAmount": 1,
      "inactiveBaseAmount": 1,
      "inactivePackagedAmount": 1,
      "material": "string",
      "owner": "string",
      "packaging": "string",
      "project": "string",
      "softAllocatedBaseAmount": 1,
      "softAllocatedPackagedAmount": 1,
      "totalBaseAmount": 1,
      "totalPackagedAmount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availableBaseAmount` | number |  |
| `availablePackagedAmount` | number |  |
| `basePackaging` | string |  |
| `basePackagingAmount` | number |  |
| `inactiveBaseAmount` | number |  |
| `inactivePackagedAmount` | number |  |
| `material` | string |  |
| `owner` | string |  |
| `packaging` | string |  |
| `project` | string |  |
| `softAllocatedBaseAmount` | number |  |
| `softAllocatedPackagedAmount` | number |  |
| `totalBaseAmount` | number |  |
| `totalPackagedAmount` | number |  |

## Native endpoint

Through the native DateX (Legacy) API, this operation is `POST inventory_availability/get` (base URL `https://{{credentials.environment}}.wavelength.host/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-available-inventory.md) for the provider-specific parameters and requirements.

