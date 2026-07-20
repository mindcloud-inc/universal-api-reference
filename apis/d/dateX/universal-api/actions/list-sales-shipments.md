# DateX (Legacy): List Sales Shipments



```
GET https://connect.mindcloud.co/v1/universal/dateX/latest/actions/list-sales-shipments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DateX (Legacy) `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dateX/latest/actions/list-sales-shipments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dateX/latest/actions/list-sales-shipments?${params}`, {
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
| `exclude.user_defined_fields` | boolean | no |  |
| `filters` | object | no |  |
| `filters.owner` | string | no |  |
| `paging.top` | number | no |  |
| `filters.project` | string | no |  |
| `paging` | object | no |  |
| `paging.skip` | number | no |  |
| `exclude_transmitted` | boolean | no | This will only return shipments that haven't been previously queries with this flag set to true - IF false will do a comprehensive search or don't want to flag orders as having been transmitted and exclude them from future queries Default: `True`. |
| `filters.warehouse` | string | no |  |
| `exclude` | object | no |  |
| `filters.status` | string | no |  |
| `filters.lookup` | string | no |  |
| `filters.order_lookup` | string | no |  |
| `filters.carrier` | string | no |  |
| `filters.carrier_service_type` | string | no |  |
| `filters.created_from` | date | no |  |
| `filters.created_to` | date | no |  |
| `filters.shipped_from` | date | no |  |
| `filters.shipped_to` | date | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "carrier": "string",
      "carrierService": "string",
      "createdOn": "string",
      "lookup": "string",
      "orderLookup": "string",
      "owner": "string",
      "project": "string",
      "shipmentId": 1,
      "shippedContents": [
        {}
      ],
      "shippedOn": "string",
      "shippingContainers": [
        {}
      ],
      "status": "string",
      "trackingIdentifier": "string",
      "warehouse": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `carrier` | string |  |
| `carrierService` | string |  |
| `createdOn` | string |  |
| `lookup` | string |  |
| `orderLookup` | string |  |
| `owner` | string |  |
| `project` | string |  |
| `shipmentId` | number |  |
| `shippedContents` | array<object> |  |
| `shippedOn` | string |  |
| `shippingContainers` | array<object> |  |
| `status` | string |  |
| `trackingIdentifier` | string |  |
| `warehouse` | string |  |

## Native endpoint

Through the native DateX (Legacy) API, this operation is `POST sales_orders/shipments/get` (base URL `https://{{credentials.environment}}.wavelength.host/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sales-shipments.md) for the provider-specific parameters and requirements.

