# Rillion Prime Web Service: List Commodities

List commodities in Rillion Prime.

```
GET https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/list-commodities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Web Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/list-commodities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/list-commodities?${params}`, {
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
| `commoditySelectParams` | object | no | Optional search filters. Leave everything empty to list all. |
| `commoditySelectParams.commodity` | string | no | Commodity name to match. |
| `commoditySelectParams.company` | list<string> | no | Company to scope the search. |
| `commoditySelectParams.supplier` | string | no | Supplier name. |
| `commoditySelectParams.maxNoOfResultRows` | number | no | Maximum number of commodities to return. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `commoditySelectParams.commodityID` | string | no |  |
| `commoditySelectParams.commodityCode` | string | no |  |
| `commoditySelectParams.itemFormName` | string | no |  |
| `commoditySelectParams.responsiblePurchaseOrderRole` | string | no |  |
| `commoditySelectParams.adviserRole1` | string | no |  |
| `commoditySelectParams.adviserRole2` | string | no |  |
| `commoditySelectParams.adviserRole3` | string | no |  |
| `commoditySelectParams.group1` | string | no |  |
| `commoditySelectParams.group2` | string | no |  |
| `commoditySelectParams.group3` | string | no |  |
| `commoditySelectParams.role` | string | no |  |
| `commoditySelectParams.supplierID` | number | no |  |
| `commoditySelectParams.countSupplier` | boolean | no |  |
| `commoditySelectParams.availableForFreetext` | string | no |  |
| `commoditySelectParams.companyIsNull` | boolean | no |  |
| `commoditySelectParams.expenditureID` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime Web Service API returns.

## Native endpoint

Through the native Rillion Prime Web Service API, this operation is `POST` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-commodities.md) for the provider-specific parameters and requirements.

