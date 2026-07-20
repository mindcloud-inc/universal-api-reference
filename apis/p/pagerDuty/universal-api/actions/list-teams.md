# PagerDuty: List Teams



```
GET https://connect.mindcloud.co/v1/universal/pagerDuty/latest/actions/list-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PagerDuty `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pagerDuty/latest/actions/list-teams?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pagerDuty/latest/actions/list-teams?${params}`, {
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
| `query` | string | no | Filter teams by a free-text search query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "defaultRole": "string",
      "description": "string",
      "htmlUrl": "https://example.com",
      "id": "string",
      "name": "Ava Chen",
      "self": "string",
      "summary": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `defaultRole` | string | The default non-member role for the team. |
| `description` | string | The description of the team. |
| `htmlUrl` | string | The PagerDuty web URL for the team. |
| `id` | string | The PagerDuty team ID. |
| `name` | string | The name of the team. |
| `self` | string | The API URL for the team. |
| `summary` | string | PagerDuty's short summary for the team. |
| `type` | string | The PagerDuty object type for the team. |

## Native endpoint

Through the native PagerDuty API, this operation is `GET /teams` (base URL `https://api.pagerduty.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-teams.md) for the provider-specific parameters and requirements.

