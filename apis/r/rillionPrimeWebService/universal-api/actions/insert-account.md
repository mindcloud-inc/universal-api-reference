# Rillion Prime Web Service: Insert Account

Insert a general ledger account into the Prime register queue.

```
POST https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Web Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "account": {},
  "account.account": "string",
  "account.keyType": 1,
  "transferFromQueue": "true"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "account": {},
    "account.account": "string",
    "account.keyType": 1,
    "transferFromQueue": "true"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `account` | object | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, Account section. |
| `account.account` | string | yes | Account |
| `account.keyType` | number | yes | Is the company included in the primary key for the record: 0=No; 1=Yes |
| `transferFromQueue` | boolean | yes | Process the record from the queue immediately. Leave true unless your Rillion contact advises otherwise. Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `account.company` | list<string> | no | Company that account is used for |
| `account.name` | string | no | Account name |
| `account.validTo` | date | no | Valid until |
| `account.vatCode` | string | no | VAT code |
| `account.allocationsAccount` | string | no | Default allocations account for the account |
| `account.isAllocationsAccount` | number | no | Can account be used as an allocations account: 0=No; 1=Yes |
| `account.vatCodeMandatory` | number | no | VatCode is mandatory when using account: 0=No; 1=Yes |
| `account.noteMandatory` | number | no | Note is mandatory when using account: 0=No; 1=Yes |
| `account.useObject1` | number | no | Is object of Type 1 to be registered: 0=Never; 1=Optional; 2=Mandatory |
| `account.useObject2` | number | no | Is object of Type 2 to be registered: 0=Never; 1=Optional; 2=Mandatory |
| `account.useObject3` | number | no | Is object of Type 3 to be registered: 0=Never; 1=Optional; 2=Mandatory |
| `account.useObject4` | number | no | Is object of Type 4 to be registered: 0=Never; 1=Optional; 2=Mandatory |
| `account.useObject5` | number | no | Is object of Type 5 to be registered: 0=Never; 1=Optional; 2=Mandatory |
| `account.useObject6` | number | no | Is object of Type 6 to be registered: 0=Never; 1=Optional; 2=Mandatory |
| `account.useObject7` | number | no | Is object of Type 7 to be registered: 0=Never; 1=Optional; 2=Mandatory |
| `account.useObject8` | number | no | Is object of Type 8 to be registered: 0=Never; 1=Optional; 2=Mandatory |
| `account.defaultObject1` | string | no | Which object of Type 1 is to be set automatically |
| `account.defaultObject2` | string | no | Which object of Type 2 is to be set automatically |
| `account.defaultObject3` | string | no | Which object of Type 3 is to be set automatically |
| `account.defaultObject4` | string | no | Which object of Type 4 is to be set automatically |
| `account.defaultObject5` | string | no | Which object of Type 5 is to be set automatically |
| `account.defaultObject6` | string | no | Which object of Type 6 is to be set automatically |
| `account.defaultObject7` | string | no | Which object of Type 7 is to be set automatically |
| `account.defaultObject8` | string | no | Which object of Type 8 is to be set automatically |
| `account.group1` | string | no | Free field of Type 1 |
| `account.group2` | string | no | Free field of Type 2 |
| `account.group3` | string | no | Free field of Type 3 |
| `account.remove` | number | no |  |
| `account.externalId` | string | no |  |
| `account.externalSource` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime Web Service API returns.

## Native endpoint

Through the native Rillion Prime Web Service API, this operation is `POST` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-account.md) for the provider-specific parameters and requirements.

