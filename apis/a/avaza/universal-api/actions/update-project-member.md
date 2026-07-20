# Avaza: Update Project Member

Updates an existing project member in Avaza.

```
PUT https://connect.mindcloud.co/v1/universal/avaza/latest/actions/update-project-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avaza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/avaza/latest/actions/update-project-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectidfk": 1,
  "useridfk": 1,
  "fieldstoupdate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avaza/latest/actions/update-project-member', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectidfk": 1,
    "useridfk": 1,
    "fieldstoupdate": "string"
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
| `projectidfk` | number | yes | Required. The ProjectID |
| `useridfk` | number | yes | Required. The UserID |
| `fieldstoupdate` | list<string> | yes | A string array of field names to be updated. |
| `costamount` | number | no | A new Cost Amount. Defaults to null. |
| `rateamount` | number | no | A new Rate Amount. Defaults to null. |
| `budgetamount` | number | no | A new Budget Amount. Defaults to null. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Avaza API returns.

## Native endpoint

Through the native Avaza API, this operation is `PUT /api/ProjectMember` (base URL `https://api.avaza.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project-member.md) for the provider-specific parameters and requirements.

