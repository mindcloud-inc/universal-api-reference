# Cloudsmith: Delete Organization Team



```
DELETE https://connect.mindcloud.co/v1/universal/cloudsmith/latest/actions/delete-organization-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudsmith `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/cloudsmith/latest/actions/delete-organization-team?connectionId=$CONNECTION_ID&org=string&team=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "org": "string",
  "team": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudsmith/latest/actions/delete-organization-team?${params}`, {
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
| `org` | string | yes | Organization slug. |
| `team` | string | yes | Team slug. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cloudsmith API returns.

## Native endpoint

Through the native Cloudsmith API, this operation is `DELETE /orgs/:org/teams/:team/` (base URL `https://api.cloudsmith.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-organization-team.md) for the provider-specific parameters and requirements.

