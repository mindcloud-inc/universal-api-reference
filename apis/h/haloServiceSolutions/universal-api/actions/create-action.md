# Halo Service Solutions: Create Action

Creates a new action in Halo Service Solutions.

```
POST https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/create-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Halo Service Solutions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/create-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ticket_id": 1,
  "outcome": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/create-action', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ticket_id": 1,
    "outcome": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ticket_id` | number | yes |  |
| `outcome` | string | yes |  |
| `note` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionby_agent_id": 1,
      "actiondatecreated": "2026-05-07T12:00:00.000Z",
      "datetime": "2026-05-07T12:00:00.000Z",
      "guid": "string",
      "id": 1,
      "new_status": 1,
      "note": "string",
      "old_status": 1,
      "outcome": "string",
      "ticket_id": 1,
      "unread": 1,
      "who": "string",
      "who_agentid": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionby_agent_id` | number |  |
| `actiondatecreated` | date |  |
| `datetime` | date |  |
| `guid` | string |  |
| `id` | number |  |
| `new_status` | number |  |
| `note` | string |  |
| `old_status` | number |  |
| `outcome` | string |  |
| `ticket_id` | number |  |
| `unread` | number |  |
| `who` | string |  |
| `who_agentid` | number |  |

## Native endpoint

Through the native Halo Service Solutions API, this operation is `POST /Actions` (base URL `https://mindcloud.halopsa.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-action.md) for the provider-specific parameters and requirements.

