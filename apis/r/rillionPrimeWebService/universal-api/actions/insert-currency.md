# Rillion Prime Web Service: Insert Currency

Insert a currency exchange rate into the Prime register queue.

```
POST https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-currency
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Web Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-currency" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "currency": {},
  "currency.baseCurrency": "string",
  "currency.currency": "string",
  "currency.buyingRate": 1,
  "transferFromQueue": "true"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-currency', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "currency": {},
    "currency.baseCurrency": "string",
    "currency.currency": "string",
    "currency.buyingRate": 1,
    "transferFromQueue": "true"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `currency` | object | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, Currency section. |
| `currency.baseCurrency` | string | yes | Currency for accounting purpose |
| `currency.currency` | string | yes | Currency |
| `currency.buyingRate` | number | yes | Buying rate |
| `transferFromQueue` | boolean | yes | Process the record from the queue immediately. Leave true unless your Rillion contact advises otherwise. Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `currency.fromAccountCodingDate` | date | no | Date from which exchange rate to be used |
| `currency.group1` | string | no | Free field of Type 1 |
| `currency.group2` | string | no | Free field of Type 2 |
| `currency.group3` | string | no | Free field of Type 3 |
| `currency.company` | list<string> | no | Company for the currency |
| `currency.keyType` | number | no | Is the company included in the primary key for the record: 0=No; 1=Yes |
| `currency.externalId` | string | no |  |
| `currency.externalSource` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime Web Service API returns.

## Native endpoint

Through the native Rillion Prime Web Service API, this operation is `POST` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-currency.md) for the provider-specific parameters and requirements.

