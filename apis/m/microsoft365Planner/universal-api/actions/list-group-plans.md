# Microsoft 365 Planner: List Group Plans



```
GET https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/list-group-plans
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Planner `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/list-group-plans?connectionId=$CONNECTION_ID&limit=25&offset=0&groupId=9b1f3c7a-1234-4abc-9def-123456789abc" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "groupId": "9b1f3c7a-1234-4abc-9def-123456789abc"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/list-group-plans?${params}`, {
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
| `groupId` | string | yes | Microsoft 365 group ID whose Planner plans should be listed. Example: `9b1f3c7a-1234-4abc-9def-123456789abc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "owner": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdDateTime` | date |  |
| `id` | string |  |
| `owner` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Microsoft 365 Planner API, this operation is `GET /v1.0/groups/{{groupId}}/planner/plans` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-group-plans.md) for the provider-specific parameters and requirements.

