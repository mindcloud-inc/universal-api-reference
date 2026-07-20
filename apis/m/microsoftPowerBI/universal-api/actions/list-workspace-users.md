# Microsoft Power BI: List Workspace Users



```
GET https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/list-workspace-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/list-workspace-users?connectionId=$CONNECTION_ID&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/list-workspace-users?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "displayName": "Ava Chen",
      "emailAddress": "ava@example.com",
      "graphId": "string",
      "groupUserAccessRight": "string",
      "identifier": "string",
      "principalType": "string",
      "userType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayName` | string | Display name of the principal. |
| `emailAddress` | string | Email address of the user. |
| `graphId` | string | Identifier of the principal in Microsoft Graph. |
| `groupUserAccessRight` | string | The access right that the principal has on the workspace. |
| `identifier` | string | Identifier of the principal. |
| `principalType` | string | The principal type. |
| `userType` | string | Type of the user. |

## Native endpoint

Through the native Microsoft Power BI API, this operation is `GET groups/[:groupId]/users` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspace-users.md) for the provider-specific parameters and requirements.

