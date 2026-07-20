# Aspire: List Inventory Locations

Retrieves inventory locations from your Aspire account.

```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-inventory-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-inventory-locations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-inventory-locations?${params}`, {
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
| `expand` | string | no |  |
| `filter` | string | no |  |
| `orderBy` | string | no |  |
| `select` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "addressID": 1,
      "addressLine1": "string",
      "addressLine2": {},
      "branchID": 1,
      "branchName": "Ava Chen",
      "city": "string",
      "defaultLocation": true,
      "inventoryLocationID": 1,
      "stateProvinceCode": "string",
      "zipCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `addressID` | number |  |
| `addressLine1` | string |  |
| `addressLine2` | object |  |
| `branchID` | number |  |
| `branchName` | string |  |
| `city` | string |  |
| `defaultLocation` | boolean |  |
| `inventoryLocationID` | number |  |
| `stateProvinceCode` | string |  |
| `zipCode` | string |  |

## Native endpoint

Through the native Aspire API, this operation is `GET InventoryLocations` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-inventory-locations.md) for the provider-specific parameters and requirements.

