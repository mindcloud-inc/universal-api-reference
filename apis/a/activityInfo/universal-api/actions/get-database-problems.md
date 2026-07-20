# ActivityInfo: Get Database Problems

Retrieves reported database problems from ActivityInfo.

```
GET https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/get-database-problems
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActivityInfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/get-database-problems?connectionId=$CONNECTION_ID&databaseId=string&typeFilter%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "string",
  "typeFilter[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/get-database-problems?${params}`, {
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
| `typeFilter[]` | array<string> | yes | Problem types to include. |
| `statusFilter` | string | no | Problem status to include. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionDescription": "string",
      "description": "string",
      "formId": "string",
      "formLabel": "string",
      "id": "string",
      "status": "string",
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
| `description` | string | Problem description. |
| `formId` | string | Form ID. |
| `formLabel` | string | Form label. |
| `id` | string | Problem ID. |
| `status` | string | Problem status. |
| `time` | number | Problem time. |
| `type` | string | Problem type. |
| `userRef` | object | User reference. |

## Native endpoint

Through the native ActivityInfo API, this operation is `POST /resources/databases/:databaseId/problems` (base URL `https://www.activityinfo.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-database-problems.md) for the provider-specific parameters and requirements.

