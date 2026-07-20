# Clockify: List Assignments

Lists all scheduling assignments in Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-assignments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-assignments?connectionId=$CONNECTION_ID&end=string&start=string&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "end": "string",
  "start": "string",
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-assignments?${params}`, {
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
| `end` | string | yes |  |
| `name` | string | no |  |
| `page` | number | no |  |
| `pageSize` | number | no |  |
| `sortColumn` | list | no | One of: `ID`, `PROJECT`, `USER`. |
| `sortOrder` | list | no | One of: `ASCENDING`, `DESCENDING`. |
| `start` | string | yes |  |
| `workspaceId` | list<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[]` | array<object> |  |
| `items[].billable` | boolean |  |
| `items[].clientId` | string |  |
| `items[].clientName` | string |  |
| `items[].hoursPerDay` | number |  |
| `items[].id` | string |  |
| `items[].note` | string |  |
| `items[].period` | object |  |
| `items[].period.end` | date |  |
| `items[].period.start` | date |  |
| `items[].projectArchived` | boolean |  |
| `items[].projectBillable` | boolean |  |
| `items[].projectColor` | string |  |
| `items[].projectId` | string |  |
| `items[].projectName` | string |  |
| `items[].startTime` | string |  |
| `items[].userId` | string |  |
| `items[].userName` | string |  |
| `items[].workspaceId` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `GET workspaces/:workspaceId/scheduling/assignments/all` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-assignments.md) for the provider-specific parameters and requirements.

