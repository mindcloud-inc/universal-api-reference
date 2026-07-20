# NeetoCal: Get Team Member

Retrieves a team member from NeetoCal.

```
GET https://connect.mindcloud.co/v1/universal/neetoCal/latest/actions/get-team-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeetoCal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neetoCal/latest/actions/get-team-member?connectionId=$CONNECTION_ID&team_member_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "team_member_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neetoCal/latest/actions/get-team-member?${params}`, {
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
| `team_member_id` | string | yes | The NeetoCal team member ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NeetoCal API returns.

## Native endpoint

Through the native NeetoCal API, this operation is `GET /team-members/:team_member_id` (base URL `https://{{credentials.subdomain}}.neetocal.com/api/external/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team-member.md) for the provider-specific parameters and requirements.

