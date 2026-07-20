# Logiwa Legacy WMS: List Products



```
GET https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Logiwa Legacy WMS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logiwaLegacyWMS/latest/actions/list-products?${params}`, {
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
| `barcodeSearch` | string | no | Barcode of inventory item |
| `code` | string | no | Depositor (client) description of inventory item |
| `description` | string | no | Description of inventory item |
| `depositorDescription` | string | no | Depositor (client) description of inventory item |
| `lastModifiedDateStart` | date | no | Last modified date may be filtered within this range - Start |
| `lastModifiedDateEnd` | date | no | Last modified date may be filtered within this range - End |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Logiwa Legacy WMS API returns.

## Native endpoint

Through the native Logiwa Legacy WMS API, this operation is `POST en/api/IntegrationApi/InventoryItemSearch` (base URL `https://{{credentials.uRL}}.logiwa.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

