# Microsoft Power BI: Groups DeleteUserAsAdmin



```
DELETE https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/admin-groups-deleteuser-as-admin
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/admin-groups-deleteuser-as-admin?connectionId=$CONNECTION_ID&groupId=string&user=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "string",
  "user": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/admin-groups-deleteuser-as-admin?${params}`, {
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
| `groupId` | string | yes | The workspace ID. |
| `user` | string | yes | The user principal name (UPN) of the user or group object Id of the group or app object Id of the service principal to delete. |
| `isGroup` | boolean | no | Whether a given user is a group or not. This parameter is required when user to delete is group. |
| `profileId` | string | no | The service principal profile ID to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `DELETE admin/groups/[:groupId]/users/[:user]` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/admin-groups-deleteuser-as-admin.md) for the provider-specific parameters and requirements.

