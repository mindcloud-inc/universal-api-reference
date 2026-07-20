# Zoho Assist: Delete Unattended Group

Deletes existing unattended computer groups from Zoho Assist.

```
DELETE https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/delete-unattended-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Assist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/delete-unattended-group?connectionId=$CONNECTION_ID&groupList%5B%5D=string&departmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupList[]": "string",
  "departmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/delete-unattended-group?${params}`, {
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
| `groupList[]` | array<string> | yes | List of unattended group IDs to delete. |
| `departmentId` | string | yes | Department in which the listed groups should be deleted. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zoho Assist API returns.

## Native endpoint

Through the native Zoho Assist API, this operation is `DELETE /unattended_computer/group` (base URL `https://assist.zoho.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-unattended-group.md) for the provider-specific parameters and requirements.

