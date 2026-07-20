# DateX (Legacy): List Materials



```
GET https://connect.mindcloud.co/v1/universal/dateX/latest/actions/list-materials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DateX (Legacy) `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dateX/latest/actions/list-materials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dateX/latest/actions/list-materials?${params}`, {
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
| `filters` | object | no |  |
| `filters.owner[]` | array<string> | no |  |
| `filters.project[]` | array<string> | no |  |
| `filters.status[]` | array<string> | no |  |
| `filters.lookup[]` | array<string> | no | An Array of lookup fields |
| `filters.globalMaterialName[]` | array<string> | no |  |
| `filters.materialName[]` | array<string> | no |  |
| `filters.materialGroup[]` | array<string> | no |  |
| `filters.materialId[]` | array<number> | no |  |
| `filters.upc[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "isFixedWeight": true,
      "isLotControlled": true,
      "isSerialControlled": true,
      "lookup": "string",
      "materialGroup": "string",
      "materialId": 1,
      "name": "Ava Chen",
      "owner": "string",
      "packagings": [
        {}
      ],
      "project": "string",
      "shelfLife": 1,
      "standardCost": 1,
      "standardPrice": 1,
      "status": "string",
      "storageCategory": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `isFixedWeight` | boolean |  |
| `isLotControlled` | boolean |  |
| `isSerialControlled` | boolean |  |
| `lookup` | string |  |
| `materialGroup` | string |  |
| `materialId` | number |  |
| `name` | string |  |
| `owner` | string |  |
| `packagings` | array<object> |  |
| `project` | string |  |
| `shelfLife` | number |  |
| `standardCost` | number |  |
| `standardPrice` | number |  |
| `status` | string |  |
| `storageCategory` | string |  |

## Native endpoint

Through the native DateX (Legacy) API, this operation is `POST materials/get` (base URL `https://{{credentials.environment}}.wavelength.host/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-materials.md) for the provider-specific parameters and requirements.

