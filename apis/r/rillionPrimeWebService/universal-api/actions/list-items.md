# Rillion Prime Web Service: List Items

List purchasing items in Rillion Prime.

```
GET https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/list-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Web Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/list-items?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/list-items?${params}`, {
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
| `itemSelectParams` | object | no | Optional search filters. Leave everything empty to list all. |
| `itemSelectParams.searchAll` | string | no | Free-text search across the item catalog. |
| `itemSelectParams.company` | list<string> | no | Company to scope the search. |
| `itemSelectParams.supplier` | string | no | Supplier ID. |
| `itemSelectParams.description` | string | no | Match on item description. |
| `itemSelectParams.onlyInCatalogue` | boolean | no | Only items in the catalogue. |
| `itemSelectParams.maxNoOfResultRows` | number | no | Maximum number of items to return. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `itemSelectParams.supplierName` | string | no |  |
| `itemSelectParams.item` | string | no | Item identifier. |
| `itemSelectParams.itemID` | string | no |  |
| `itemSelectParams.itemCatalogue` | string | no |  |
| `itemSelectParams.note` | string | no |  |
| `itemSelectParams.supplierItem` | string | no |  |
| `itemSelectParams.responsiblePurchaseOrderRole` | string | no |  |
| `itemSelectParams.commodity` | string | no |  |
| `itemSelectParams.commodityCode` | string | no |  |
| `itemSelectParams.manufacturer` | string | no |  |
| `itemSelectParams.manufacturerItem` | string | no |  |
| `itemSelectParams.contractNo` | string | no |  |
| `itemSelectParams.blocked` | string | no |  |
| `itemSelectParams.bestBuy` | string | no |  |
| `itemSelectParams.validFrom` | date | no |  |
| `itemSelectParams.validTo` | date | no |  |
| `itemSelectParams.group1` | string | no |  |
| `itemSelectParams.group2` | string | no |  |
| `itemSelectParams.group3` | string | no |  |
| `itemSelectParams.externalId` | string | no |  |
| `itemSelectParams.externalSource` | string | no |  |
| `itemSelectParams.onlyFavourite` | boolean | no |  |
| `itemSelectParams.onlyBestBuy` | boolean | no |  |
| `itemSelectParams.onlyHaveContract` | boolean | no |  |
| `itemSelectParams.onlyEcoLabel` | boolean | no |  |
| `itemSelectParams.filterByPrice` | boolean | no |  |
| `itemSelectParams.filterByPriceMin` | number | no |  |
| `itemSelectParams.filterByPriceMax` | number | no |  |
| `itemSelectParams.companyIsNull` | boolean | no |  |
| `itemSelectParams.expenditureId` | number | no |  |
| `itemSelectParams.itemFormName` | string | no |  |
| `itemSelectParams.itemTypeLinksFrom` | number | no |  |
| `itemSelectParams.itemTypeLinksTo` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime Web Service API returns.

## Native endpoint

Through the native Rillion Prime Web Service API, this operation is `POST` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-items.md) for the provider-specific parameters and requirements.

