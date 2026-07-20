# Zeplin: Remove Project Member

Removes a member from a Zeplin project.

```
DELETE https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/remove-project-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/remove-project-member?connectionId=$CONNECTION_ID&projectId=string&memberId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "memberId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/remove-project-member?${params}`, {
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
| `projectId` | string | yes | Project id |
| `memberId` | string | yes | Member id |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zeplin API returns.

## Native endpoint

Through the native Zeplin API, this operation is `DELETE /projects/{project_id}/members/{member_id}` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-project-member.md) for the provider-specific parameters and requirements.

