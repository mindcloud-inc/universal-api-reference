# Avaza: Create Project Member

Creates a new project member in Avaza.

```
POST https://connect.mindcloud.co/v1/universal/avaza/latest/actions/create-project-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avaza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/avaza/latest/actions/create-project-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avaza/latest/actions/create-project-member', {
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
| `istimesheetallowed` | boolean | no |  |
| `istimesheetapprover` | boolean | no |  |
| `isexpenseapprover` | boolean | no |  |
| `istimesheetapprovalrequired` | boolean | no |  |
| `cancreatetasks` | boolean | no |  |
| `candeletetasks` | boolean | no |  |
| `cancommentontasks` | boolean | no |  |
| `canupdatetasks` | boolean | no |  |
| `projectidfk` | number | no | Required. The ProjectID |
| `useridfk` | number | no | Required. The UserID to assign |
| `costamount` | number | no | Optional. If not provided, defaults to the User's default Cost Amount. |
| `rateamount` | number | no | Optional. If not provided, defaults to the User's default Rate Amount. |
| `budgetamount` | number | no | Optional |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Avaza API returns.

## Native endpoint

Through the native Avaza API, this operation is `POST /api/ProjectMember` (base URL `https://api.avaza.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project-member.md) for the provider-specific parameters and requirements.

