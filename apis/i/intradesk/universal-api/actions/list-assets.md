# Intradesk: List Assets

Retrieves assets from Intradesk.

```
GET https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/list-assets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intradesk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/list-assets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/list-assets?${params}`, {
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
      "assetAddress": {},
      "assetAddressId": 1,
      "client": {},
      "clientId": 1,
      "description": "string",
      "id": 1,
      "inventoryNumber": "string",
      "isArchived": true,
      "isNameStartsFromInventory": true,
      "name": "Ava Chen",
      "nameManually": "Ava Chen",
      "ownerId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assetAddress` | object |  |
| `assetAddressId` | number |  |
| `client` | object |  |
| `clientId` | number |  |
| `description` | string |  |
| `id` | number |  |
| `inventoryNumber` | string |  |
| `isArchived` | boolean |  |
| `isNameStartsFromInventory` | boolean |  |
| `name` | string |  |
| `nameManually` | string |  |
| `ownerId` | number |  |

## Native endpoint

Through the native Intradesk API, this operation is `GET /settings/odata/v1/Assets` (base URL `https://apigw.intradesk.ru`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-assets.md) for the provider-specific parameters and requirements.

