# Spike.sh: Create Service

Creates a new service in Spike.sh.

```
POST https://connect.mindcloud.co/v1/universal/spikesh/latest/actions/create-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spike.sh `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/spikesh/latest/actions/create-service" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "teamId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/spikesh/latest/actions/create-service', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "teamId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `desc` | string | no | Service description. |
| `name` | string | yes | Service name. |
| `teamId` | string | yes | Spike.sh team ID used to populate the x-team-id request header for team-scoped endpoints. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Spike.sh API returns.

## Native endpoint

Through the native Spike.sh API, this operation is `POST /services/create` (base URL `https://api.spike.sh`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-service.md) for the provider-specific parameters and requirements.

