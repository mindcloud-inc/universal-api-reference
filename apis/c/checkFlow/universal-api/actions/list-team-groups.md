# CheckFlow: List Team Groups



```
GET https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/list-team-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CheckFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/list-team-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/list-team-groups?${params}`, {
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
| `nameContains` | string | no | Filters results to groups whose name contains this string. Leave empty to return all. Example: `Operations`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assigneeId": 1,
      "assigneeName": "Ava Chen",
      "assigneeType": 1,
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assigneeId` | number | Assignee identifier for the group. |
| `assigneeName` | string | Group display name. |
| `assigneeType` | number | Assignee type value for groups. |
| `id` | number | Group identifier. |

## Native endpoint

Through the native CheckFlow API, this operation is `GET /api/team/groups` (base URL `https://app.checkflow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-team-groups.md) for the provider-specific parameters and requirements.

