# ActivityInfo: List Database User Grants On Resource

Retrieves user grants for an ActivityInfo database resource.

```
GET https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/list-database-user-grants-on-resource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActivityInfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/list-database-user-grants-on-resource?connectionId=$CONNECTION_ID&databaseId=string&resourceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "string",
  "resourceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/list-database-user-grants-on-resource?${params}`, {
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
| `databaseId` | string | yes | ActivityInfo database ID. |
| `resourceId` | string | yes | ActivityInfo database resource ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activationStatus": "string",
      "databaseId": "string",
      "email": "ava@example.com",
      "name": "Ava Chen",
      "role": {},
      "userId": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activationStatus` | string | User activation status. |
| `databaseId` | string | Database ID. |
| `email` | string | User email. |
| `name` | string | User name. |
| `role` | object | Role/grant information. |
| `userId` | string | User ID. |
| `version` | number | Grant version. |

## Native endpoint

Through the native ActivityInfo API, this operation is `GET /resources/databases/:databaseId/resources/:resourceId/grants` (base URL `https://www.activityinfo.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-database-user-grants-on-resource.md) for the provider-specific parameters and requirements.

