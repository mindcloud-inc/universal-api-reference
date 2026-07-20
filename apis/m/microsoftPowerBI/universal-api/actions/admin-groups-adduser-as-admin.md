# Microsoft Power BI: Groups AddUserAsAdmin



```
POST https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/admin-groups-adduser-as-admin
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/admin-groups-adduser-as-admin" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string",
  "groupUserAccessRight": "string",
  "identifier": "string",
  "principalType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/admin-groups-adduser-as-admin', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string",
    "groupUserAccessRight": "string",
    "identifier": "string",
    "principalType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupId` | string | yes | The workspace ID |
| `groupUserAccessRight` | list | yes | The access right (permission level) that a user has on the workspace |
| `identifier` | string | yes | Identifier of the principal |
| `principalType` | list | yes | The principal type |
| `displayName` | string | no | Display name of the principal |
| `emailAddress` | string | no | Email address of the user |
| `graphId` | string | no | Identifier of the principal in Microsoft Graph. Only available for admin APIs. |
| `profile` | object | no | A Power BI service principal profile. Only relevant for Power BI Embedded multi-tenancy solution. |
| `userType` | string | no | Type of the user. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `POST admin/groups/[:groupId]/users` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/admin-groups-adduser-as-admin.md) for the provider-specific parameters and requirements.

