# Rillion Prime Web Service: Insert Period

Insert an accounting period into the Prime register queue.

```
POST https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-period
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Web Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-period" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "period": {},
  "period.year": 1,
  "period.period": 1,
  "period.name": "Ava Chen",
  "period.startDate": "2026-05-07T12:00:00.000Z",
  "period.endDate": "2026-05-07T12:00:00.000Z",
  "transferFromQueue": "true"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-period', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "period": {},
    "period.year": 1,
    "period.period": 1,
    "period.name": "Ava Chen",
    "period.startDate": "2026-05-07T12:00:00.000Z",
    "period.endDate": "2026-05-07T12:00:00.000Z",
    "transferFromQueue": "true"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `period` | object | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, Period section. |
| `period.year` | number | yes | Year (1-9999) |
| `period.period` | number | yes | Period (1-40) |
| `period.name` | string | yes | Name of period |
| `period.startDate` | date | yes | Start date for period |
| `period.endDate` | date | yes | End date for period |
| `transferFromQueue` | boolean | yes | Process the record from the queue immediately. Leave true unless your Rillion contact advises otherwise. Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `period.company` | list<string> | no | Company to which the period belongs |
| `period.closed` | number | no | Closed: 0=No; 1=Yes |
| `period.group1` | string | no | Free field of Type 1 |
| `period.group2` | string | no | Free field of Type 2 |
| `period.group3` | string | no | Free field of Type 3 |
| `period.keyType` | number | no | Is the company included in the primary key for the record: 0=No; 1=Yes |
| `period.externalId` | string | no |  |
| `period.externalSource` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime Web Service API returns.

## Native endpoint

Through the native Rillion Prime Web Service API, this operation is `POST` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-period.md) for the provider-specific parameters and requirements.

