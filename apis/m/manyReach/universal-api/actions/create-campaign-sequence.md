# ManyReach: Create Campaign Sequence

Creates a sequence for a campaign in ManyReach.

```
POST https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/create-campaign-sequence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/create-campaign-sequence" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/create-campaign-sequence', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no | Campaign ID. |
| `name` | string | yes | Sequence name. |

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

Through the native ManyReach API, this operation is `POST https://api.manyreach.com/api/v2/campaigns/:id/sequences` (base URL `https://api.manyreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign-sequence.md) for the provider-specific parameters and requirements.

