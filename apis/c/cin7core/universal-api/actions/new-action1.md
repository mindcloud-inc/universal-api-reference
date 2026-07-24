# Cin7 Core: List Products



```
GET https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/new-action1
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cin7 Core `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/new-action1?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/new-action1?${params}`, {
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
| `ID` | string | no | Returns stock info of a particular product (Default: null) |
| `Name` | string | no | Only return products with product name containing specified name value (Default: null) |
| `Sku` | string | no | Only return products with product sku containing specified sku value (Default: null) |
| `ModifiedSince` | date | no | Only return Products modified since specified date (UTC time) in ISO 8601 format. (Default: null) |
| `IncludeDeprecated` | boolean | no | Returns all Products, including deprecated, if set to true. If set to false or if it is not specified then returns only active (ie. non-deprecated) Products (Default: false) |
| `IncludeBOM` | boolean | no | Include Bill Of Materials information (Default: false) |
| `IncludeSuppliers` | boolean | no | Include Suppliers information (Default: false) |
| `IncludeMovements` | boolean | no | Include Movements information (Default: false) |
| `IncludeAttachments` | boolean | no | Include Attachments information (Default: false) |
| `IncludeReorderLevels` | boolean | no | Include Reorder Levels information (Default: false) |
| `IncludeCustomPrices` | boolean | no | Include Customer specific Prices (Default: false) |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cin7 Core API returns.

## Native endpoint

Through the native Cin7 Core API, this operation is `GET product` (base URL `https://inventory.dearsystems.com/externalapi/v2/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/new-action1.md) for the provider-specific parameters and requirements.

