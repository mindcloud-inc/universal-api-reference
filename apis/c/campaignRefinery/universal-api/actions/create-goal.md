# Campaign Refinery: Create Goal

Creates a new goal in Campaign Refinery.

```
POST https://connect.mindcloud.co/v1/universal/campaignRefinery/latest/actions/create-goal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campaign Refinery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/campaignRefinery/latest/actions/create-goal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/campaignRefinery/latest/actions/create-goal', {
  method: 'POST',
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
| `name` | string | no | The goal's name. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Campaign Refinery API returns.

## Native endpoint

Through the native Campaign Refinery API, this operation is `POST /goals/create-goal` (base URL `https://app.campaignrefinery.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-goal.md) for the provider-specific parameters and requirements.

