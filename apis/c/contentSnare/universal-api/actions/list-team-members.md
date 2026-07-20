# Content Snare: List Team Members

Retrieves team members from Content Snare.

```
GET https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/list-team-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Content Snare `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/list-team-members?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/list-team-members?${params}`, {
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
| `q` | string | no | String to search in the values specified in the parameter `q_by[]` |
| `qBy[]` | array<string> | no | Specifies list of values where string from the parameter `q` will be searched. If it isn't set then the default list is used.<br><b>Examples:</b> q_by[]=full_name&q_by[]=phone |
| `sortBy` | string | no | Specifies value for sorting |
| `sortDirection` | string | no | Specifies direction for sorting |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "avatar": "string",
      "company_name": "Ava Chen",
      "email": "ava@example.com",
      "full_name": "Ava Chen",
      "id": "string",
      "phone": "string",
      "role": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `avatar` | string |  |
| `company_name` | string |  |
| `email` | string |  |
| `full_name` | string |  |
| `id` | string |  |
| `phone` | string |  |
| `role` | string |  |

## Native endpoint

Through the native Content Snare API, this operation is `GET /partner_api/v1/team_members` (base URL `https://api.contentsnare.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-team-members.md) for the provider-specific parameters and requirements.

