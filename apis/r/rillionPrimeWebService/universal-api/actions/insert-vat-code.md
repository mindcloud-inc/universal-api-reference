# Rillion Prime Web Service: Insert VAT Code

Insert a VAT code into the Prime register queue.

```
POST https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-vat-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Web Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-vat-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "vatCode": {},
  "vatCode.vatCode": "string",
  "vatCode.name": "Ava Chen",
  "transferFromQueue": "true"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-vat-code', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "vatCode": {},
    "vatCode.vatCode": "string",
    "vatCode.name": "Ava Chen",
    "transferFromQueue": "true"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `vatCode` | object | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, VatCode section. |
| `vatCode.vatCode` | string | yes | VAT code |
| `vatCode.name` | string | yes | VAT code name |
| `transferFromQueue` | boolean | yes | Process the record from the queue immediately. Leave true unless your Rillion contact advises otherwise. Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `vatCode.company` | list<string> | no | Company to which VAT code belongs |
| `vatCode.validTo` | date | no | A valid to date for vatcodes |
| `vatCode.account` | string | no | VAT account to which VAT code belongs |
| `vatCode.percentage` | number | no | VAT rate |
| `vatCode.vatDeductionAccount` | string | no | Account for VAT remainder |
| `vatCode.group1` | string | no | Free group 1 |
| `vatCode.group2` | string | no | Free group 2 |
| `vatCode.group3` | string | no | Free group 3 |
| `vatCode.keyType` | number | no | Is the company included in the primary key for the record: 0=No; 1=Yes |
| `vatCode.externalId` | string | no |  |
| `vatCode.externalSource` | string | no |  |
| `vatCode.fromDate` | date | no | From invoice date the VAT percentage shall be used. Support of SAF-T |
| `vatCode.deductionalVatPercentage` | number | no | Percentage of deductible VAT |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime Web Service API returns.

## Native endpoint

Through the native Rillion Prime Web Service API, this operation is `POST` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-vat-code.md) for the provider-specific parameters and requirements.

