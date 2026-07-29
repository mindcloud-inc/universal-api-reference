# Rillion Prime Web Service: Insert Commodity

Insert a commodity into the Prime register queue.

```
POST https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-commodity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Web Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-commodity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "commodity": {},
  "commodity.commodity": "string",
  "commodity.expenditureAmount": 1,
  "transferFromQueue": "true"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-commodity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "commodity": {},
    "commodity.commodity": "string",
    "commodity.expenditureAmount": 1,
    "transferFromQueue": "true"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `commodity` | object | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, Commodity section. |
| `commodity.commodity` | string | yes | The name of the commodity |
| `commodity.expenditureAmount` | number | yes | Amount |
| `transferFromQueue` | boolean | yes | Process the record from the queue immediately. Leave true unless your Rillion contact advises otherwise. Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `commodity.rolePermission` | string | no |  |
| `commodity.linkToSupplier` | string | no |  |
| `commodity.advisoryRole1` | string | no |  |
| `commodity.advisoryRole2` | string | no |  |
| `commodity.advisoryRole3` | string | no |  |
| `commodity.productGroupName` | string | no |  |
| `commodity.itemFormName` | string | no |  |
| `commodity.availableForFreetext` | boolean | no |  |
| `commodity.commodityCode` | string | no | CommodityCode |
| `commodity.company` | list<string> | no | Company that commodity is linked to |
| `commodity.buyersHelp` | boolean | no | ResponsiblePurchaseOrderRole inserted last in the flow: 0=No, 1=Yes |
| `commodity.responsiblePurchaseOrderRole` | string | no | Responsible PurchaseOrderRole |
| `commodity.purchaseOrderMatchType` | number | no | PurchaseOrderMatchType 0=Number;1=Amount |
| `commodity.account` | string | no | Account |
| `commodity.vatCode` | string | no | VAT Codes |
| `commodity.group1` | string | no | Free field of Type1 |
| `commodity.group2` | string | no | Free field of Type2 |
| `commodity.group3` | string | no | Free field of Type3 |
| `commodity.externalId` | string | no |  |
| `commodity.externalSource` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime Web Service API returns.

## Native endpoint

Through the native Rillion Prime Web Service API, this operation is `POST` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-commodity.md) for the provider-specific parameters and requirements.

