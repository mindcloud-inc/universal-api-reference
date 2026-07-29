# Rillion Prime Web Service: Insert Company

Insert a company into the Prime register queue.

```
POST https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Web Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "company": {},
  "company.company": "string",
  "company.name": "Ava Chen",
  "transferFromQueue": "true"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "company": {},
    "company.company": "string",
    "company.name": "Ava Chen",
    "transferFromQueue": "true"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `company` | object | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, Company section. |
| `company.company` | list<string> | yes | Company ID |
| `company.name` | string | yes | Trade name |
| `transferFromQueue` | boolean | yes | Process the record from the queue immediately. Leave true unless your Rillion contact advises otherwise. Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `company.validTo` | date | no | Can receive invoices until this date |
| `company.invoiceSeries` | string | no | FK to invoice number series |
| `company.arrivalType` | number | no | When is the invoice to be preliminarily recorded in the ERP system: 0=Never; 1=When it is sent to the first person in the flow; 2=When the first person in the flow has approved it |
| `company.baseCurrency` | string | no | Currency for accounting purpose |
| `company.erp` | string | no | Belongs to this ERP system if several used (used for integration purposes) |
| `company.group1` | string | no | Free field of Type 1 |
| `company.group2` | string | no | Free field of Type 2 |
| `company.group3` | string | no | Free field of Type 3 |
| `company.remove` | number | no |  |
| `company.allocationSetting` | number | no | Method of distribution: 0=Distribute by From and To date; 1=Distribute by distribution type |
| `company.calculateVATAmountOnCostRow` | boolean | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime Web Service API returns.

## Native endpoint

Through the native Rillion Prime Web Service API, this operation is `POST` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-company.md) for the provider-specific parameters and requirements.

