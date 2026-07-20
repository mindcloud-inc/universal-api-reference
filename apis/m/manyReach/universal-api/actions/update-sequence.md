# ManyReach: Update Sequence

Updates an existing sequence in ManyReach.

```
PUT https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/update-sequence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/update-sequence" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/update-sequence', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no | Sequence ID. |
| `name` | string | no | Updated sequence name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conditionAction": "string",
      "conditionExtra": true,
      "conditionNegate": true,
      "conditionOperator": "string",
      "conditionReply": "string",
      "conditionTimes": 1,
      "name": "Ava Chen",
      "sequenceId": 1,
      "shortName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conditionAction` | string |  |
| `conditionExtra` | boolean |  |
| `conditionNegate` | boolean |  |
| `conditionOperator` | string |  |
| `conditionReply` | string |  |
| `conditionTimes` | number |  |
| `name` | string |  |
| `sequenceId` | number |  |
| `shortName` | string |  |

## Native endpoint

Through the native ManyReach API, this operation is `PATCH https://api.manyreach.com/api/v2/sequences/:id` (base URL `https://api.manyreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sequence.md) for the provider-specific parameters and requirements.

