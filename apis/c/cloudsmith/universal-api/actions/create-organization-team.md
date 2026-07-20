# Cloudsmith: Create Organization Team



```
POST https://connect.mindcloud.co/v1/universal/cloudsmith/latest/actions/create-organization-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudsmith `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloudsmith/latest/actions/create-organization-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "org": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloudsmith/latest/actions/create-organization-team', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "org": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `org` | string | yes | Organization slug. |
| `name` | string | yes | Team name. |
| `description` | string | no | Team description. |
| `visibility` | string | no | Team visibility. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cloudsmith API returns.

## Native endpoint

Through the native Cloudsmith API, this operation is `POST /orgs/:org/teams/` (base URL `https://api.cloudsmith.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-organization-team.md) for the provider-specific parameters and requirements.

