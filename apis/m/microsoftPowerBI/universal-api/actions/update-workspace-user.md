# Microsoft Power BI: Update Workspace User



```
PUT https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/update-workspace-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/update-workspace-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string",
  "identifier": "string",
  "principalType": "User",
  "groupUserAccessRight": "Contributor"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/update-workspace-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string",
    "identifier": "string",
    "principalType": "User",
    "groupUserAccessRight": "Contributor"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupId` | string | yes | The Power BI workspace ID. |
| `identifier` | string | yes | The user, group, or app identifier whose workspace access should be updated. |
| `principalType` | list | yes | The principal type. Default: `User`. |
| `groupUserAccessRight` | list | yes | The updated workspace access level. Default: `Contributor`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `PUT groups/[:groupId]/users` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-workspace-user.md) for the provider-specific parameters and requirements.

