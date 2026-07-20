# CleverReach: List Group Receiver Events

Retrieves receiver events for a group receiver in CleverReach.

```
GET https://connect.mindcloud.co/v1/universal/cleverReach/latest/actions/list-group-receiver-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CleverReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cleverReach/latest/actions/list-group-receiver-events?connectionId=$CONNECTION_ID&groupId=string&poolId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "string",
  "poolId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cleverReach/latest/actions/list-group-receiver-events?${params}`, {
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
| `groupId` | string | yes | Group ID. |
| `poolId` | string | yes | ID or email of receiver. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CleverReach API returns.

## Native endpoint

Through the native CleverReach API, this operation is `GET /v3/groups.json/:groupId/receivers/:poolId/events` (base URL `https://rest.cleverreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-group-receiver-events.md) for the provider-specific parameters and requirements.

