# Unleashed: List Warehouses

Retrieves warehouses from your Unleashed account.

```
GET https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/list-warehouses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unleashed `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/list-warehouses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/list-warehouses?${params}`, {
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
      "addressLine1": "string",
      "city": "string",
      "contactName": "Ava Chen",
      "country": "string",
      "guid": "string",
      "isDefault": true,
      "lastModifiedOn": "string",
      "obsolete": true,
      "phoneNumber": "string",
      "postCode": "string",
      "region": "string",
      "warehouseCode": "string",
      "warehouseName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addressLine1` | string |  |
| `city` | string |  |
| `contactName` | string |  |
| `country` | string |  |
| `guid` | string |  |
| `isDefault` | boolean |  |
| `lastModifiedOn` | string |  |
| `obsolete` | boolean |  |
| `phoneNumber` | string |  |
| `postCode` | string |  |
| `region` | string |  |
| `warehouseCode` | string |  |
| `warehouseName` | string |  |

## Native endpoint

Through the native Unleashed API, this operation is `GET /Warehouses/:pageNumber` (base URL `https://api.unleashedsoftware.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-warehouses.md) for the provider-specific parameters and requirements.

