# Saleshandy: Update Sequence Schedule



```
PUT https://connect.mindcloud.co/v1/universal/saleshandy/latest/actions/update-sequence-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Saleshandy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/saleshandy/latest/actions/update-sequence-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sequenceId": "string",
  "scheduleId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/saleshandy/latest/actions/update-sequence-schedule', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sequenceId": "string",
    "scheduleId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sequenceId` | string | yes | Sequence ID to update. |
| `scheduleId` | string | yes | Schedule ID to assign to the sequence. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "payload": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `payload` | object |  |

## Native endpoint

Through the native Saleshandy API, this operation is `PATCH /sequences/[:sequenceId]/schedule` (base URL `https://open-api.saleshandy.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sequence-schedule.md) for the provider-specific parameters and requirements.

