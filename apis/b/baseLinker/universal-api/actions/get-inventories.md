# BaseLinker: Get Inventories

Retrieves inventories from BaseLinker.

```
GET https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/get-inventories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BaseLinker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/get-inventories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/get-inventories?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "inventories": [
        {
          "defaultLanguage": "string",
          "defaultPriceGroup": 1,
          "defaultWarehouse": "string",
          "description": "string",
          "inventoryId": 1,
          "isDefault": true,
          "languages": [
            "string"
          ],
          "name": "Ava Chen",
          "priceGroups": [
            1
          ],
          "reservations": true,
          "warehouses": [
            "string"
          ]
        }
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `inventories[].defaultLanguage` | string |  |
| `inventories[].defaultPriceGroup` | number |  |
| `inventories[].defaultWarehouse` | string |  |
| `inventories[].description` | string |  |
| `inventories[].inventoryId` | number |  |
| `inventories[].isDefault` | boolean |  |
| `inventories[].languages[]` | string |  |
| `inventories[].name` | string |  |
| `inventories[].priceGroups[]` | number |  |
| `inventories[].reservations` | boolean |  |
| `inventories[].warehouses[]` | string |  |
| `status` | string |  |

## Native endpoint

Through the native BaseLinker API, this operation is `POST /connector.php` (base URL `https://api.baselinker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inventories.md) for the provider-specific parameters and requirements.

