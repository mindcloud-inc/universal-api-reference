# Halo Service Solutions: Get Action

Retrieves an action from Halo Service Solutions.

```
GET https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Halo Service Solutions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-action?connectionId=$CONNECTION_ID&id=1&ticket_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1",
  "ticket_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-action?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Action ID. |
| `ticket_id` | number | yes | The ticket id to get the action for. |

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
      "who": "string"
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

## Native endpoint

Through the native Halo Service Solutions API, this operation is `GET /Actions/:id` (base URL `https://mindcloud.halopsa.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-action.md) for the provider-specific parameters and requirements.

