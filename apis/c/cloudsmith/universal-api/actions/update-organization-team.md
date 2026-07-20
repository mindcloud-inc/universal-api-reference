# Cloudsmith: Update Organization Team



```
PUT https://connect.mindcloud.co/v1/universal/cloudsmith/latest/actions/update-organization-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudsmith `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cloudsmith/latest/actions/update-organization-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "org": "string",
  "team": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloudsmith/latest/actions/update-organization-team', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "org": "string",
    "team": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `org` | string | yes | Organization slug. |
| `team` | string | yes | Team slug. |
| `name` | string | no | Updated team name. |
| `description` | string | no | Updated team description. |
| `visibility` | string | no | Updated team visibility. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cloudsmith API returns.

## Native endpoint

Through the native Cloudsmith API, this operation is `PATCH /orgs/:org/teams/:team/` (base URL `https://api.cloudsmith.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-organization-team.md) for the provider-specific parameters and requirements.

