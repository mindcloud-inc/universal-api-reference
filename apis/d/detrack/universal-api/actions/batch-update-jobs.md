# Detrack: Batch Update Jobs

Updates multiple jobs in Detrack at once.

```
PUT https://connect.mindcloud.co/v1/universal/detrack/latest/actions/batch-update-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Detrack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/detrack/latest/actions/batch-update-jobs" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/detrack/latest/actions/batch-update-jobs', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data[]` | array<object> | yes | Array of job update objects. Each item must include do_number, date, and a nested data object with the fields to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "string",
      "doNumber": "string",
      "ok": true,
      "type": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | string |  |
| `doNumber` | string |  |
| `ok` | boolean |  |
| `type` | object |  |

## Native endpoint

Through the native Detrack API, this operation is `PUT /dn/jobs` (base URL `https://app.detrack.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-update-jobs.md) for the provider-specific parameters and requirements.

