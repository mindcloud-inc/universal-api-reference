# Scalr: Unlock Environment

Unlocks an environment in Scalr.

```
PUT https://connect.mindcloud.co/v1/universal/scalr/latest/actions/unlock-environment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scalr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/scalr/latest/actions/unlock-environment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "environment": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scalr/latest/actions/unlock-environment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "environment": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `environment` | string | yes | Scalr environment ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Scalr API returns.

## Native endpoint

Through the native Scalr API, this operation is `POST /environments/:environment/actions/unlock` (base URL `https://mindcloud.scalr.io/api/iacp/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unlock-environment.md) for the provider-specific parameters and requirements.

