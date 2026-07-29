# Rillion Prime Web Service: Insert Object

Insert an accounting object (coding dimension value) into the Prime register queue.

```
POST https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Web Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-object" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "object": {},
  "object.objectTypeNo": 1,
  "object.object": "string",
  "object.name": "Ava Chen",
  "transferFromQueue": "true"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-object', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "object": {},
    "object.objectTypeNo": 1,
    "object.object": "string",
    "object.name": "Ava Chen",
    "transferFromQueue": "true"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `object` | object | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, Object section. |
| `object.objectTypeNo` | number | yes | Object type number (1-8) |
| `object.object` | string | yes | Object |
| `object.name` | string | yes | Object name |
| `transferFromQueue` | boolean | yes | Process the record from the queue immediately. Leave true unless your Rillion contact advises otherwise. Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `object.company` | list<string> | no | Company to which object belongs |
| `object.validFrom` | date | no | Valid from |
| `object.validTo` | date | no | Valid until |
| `object.vatDeduction` | number | no | Percentage liable for VAT |
| `object.defaultObject1` | string | no | Which object of Type 1 is to be set automatically |
| `object.defaultObject2` | string | no | Which object of Type 2 is to be set automatically |
| `object.defaultObject3` | string | no | Which object of Type 3 is to be set automatically |
| `object.defaultObject4` | string | no | Which object of Type 4 is to be set automatically |
| `object.defaultObject5` | string | no | Which object of Type 5 is to be set automatically |
| `object.defaultObject6` | string | no | Which object of Type 6 is to be set automatically |
| `object.defaultObject7` | string | no | Which object of Type 7 is to be set automatically |
| `object.defaultObject8` | string | no | Which object of Type 8 is to be set automatically |
| `object.group1` | string | no | Free field of Type 1 |
| `object.group2` | string | no | Free field of Type 2 |
| `object.group3` | string | no | Free field of Type 3 |
| `object.remove` | number | no | Should record be removed: 0=No; 1=Yes |
| `object.keyType` | number | no | Is the company included in the primary key for the record: 0=No; 1=Yes |
| `object.externalId` | string | no |  |
| `object.externalSource` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime Web Service API returns.

## Native endpoint

Through the native Rillion Prime Web Service API, this operation is `POST` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-object.md) for the provider-specific parameters and requirements.

