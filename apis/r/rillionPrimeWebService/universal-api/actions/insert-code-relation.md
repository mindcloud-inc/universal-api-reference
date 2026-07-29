# Rillion Prime Web Service: Insert Code Relation

Insert a coding relation into the Prime register queue.

```
POST https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-code-relation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Web Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-code-relation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "codeRelation": {},
  "codeRelation.selectVatCode": "string",
  "transferFromQueue": "true"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-code-relation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "codeRelation": {},
    "codeRelation.selectVatCode": "string",
    "transferFromQueue": "true"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `codeRelation` | object | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, CodeRelation section. |
| `codeRelation.selectVatCode` | string | yes | Filter by object of Type 9 |
| `transferFromQueue` | boolean | yes | Process the record from the queue immediately. Leave true unless your Rillion contact advises otherwise. Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `codeRelation.company` | list<string> | no | Company that rule is linked to |
| `codeRelation.selectAccount` | string | no | Filter by account |
| `codeRelation.selectObject1` | string | no | Filter by object of Type 1 |
| `codeRelation.selectObject2` | string | no | Filter by object of Type 2 |
| `codeRelation.selectObject3` | string | no | Filter by object of Type 3 |
| `codeRelation.selectObject4` | string | no | Filter by object of Type 4 |
| `codeRelation.selectObject5` | string | no | Filter by object of Type 5 |
| `codeRelation.selectObject6` | string | no | Filter by object of Type 6 |
| `codeRelation.selectObject7` | string | no | Filter by object of Type 7 |
| `codeRelation.selectObject8` | string | no | Filter by vat code |
| `codeRelation.fromDate` | date | no | Rule active from this date |
| `codeRelation.toDate` | date | no | Rule active until this date |
| `codeRelation.blocked` | number | no | Does the rule refer to a blocked relation: 0=No; 1=Yes |
| `codeRelation.blockedMessage` | string | no | Error text if Blocked=1 |
| `codeRelation.externalId` | string | no |  |
| `codeRelation.externalSource` | string | no |  |
| `codeRelation.useAsFilter` | boolean | no | Allocation setting |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime Web Service API returns.

## Native endpoint

Through the native Rillion Prime Web Service API, this operation is `POST` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-code-relation.md) for the provider-specific parameters and requirements.

