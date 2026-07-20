# ActivityInfo: Audit Database

Retrieves audit entries for an ActivityInfo database.

```
GET https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/audit-database
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActivityInfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/audit-database?connectionId=$CONNECTION_ID&databaseId=string&typeFilter%5B%5D=string&startTime=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "string",
  "typeFilter[]": "string",
  "startTime": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/audit-database?${params}`, {
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
| `typeFilter[]` | array<string> | yes | Audit event resource types to include. |
| `startTime` | number | yes | Start time in milliseconds since epoch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionDescription": "string",
      "description": "string",
      "resourceId": "string",
      "time": 1,
      "type": "string",
      "userRef": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionDescription` | string | Action description. |
| `description` | string | Audit event description. |
| `resourceId` | string | Affected resource ID. |
| `time` | number | Audit event time. |
| `type` | string | Audit event type. |
| `userRef` | object | User responsible for the event. |

## Native endpoint

Through the native ActivityInfo API, this operation is `POST /resources/databases/:databaseId/audit` (base URL `https://www.activityinfo.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/audit-database.md) for the provider-specific parameters and requirements.

