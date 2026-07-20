# Range: List Updates

List updates with optional target, teammate, and time filters.

```
GET https://connect.mindcloud.co/v1/universal/range/latest/actions/list-updates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Range `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/range/latest/actions/list-updates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/range/latest/actions/list-updates?${params}`, {
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
| `after` | string | no | Only fetch updates after this ISO8601 time. |
| `ascending` | boolean | no | Whether to order oldest first. |
| `before` | string | no | Only fetch updates before this ISO8601 time. |
| `count` | number | no | Limit the number of updates returned. |
| `forUserId` | string | no | Fetch updates from a user's teammates. |
| `includeChildTeams` | boolean | no | Whether to include descendant-team updates. |
| `includeRefs` | boolean | no | Whether to return snippets, attachments, and users. |
| `targetId` | string | no | User, team, or organization target ID. |
| `useClientOffset` | boolean | no | Whether to localize update time to the author's calendar day. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {}
      ],
      "pagination": {},
      "snippets": [
        {}
      ],
      "updates": [
        {}
      ],
      "users": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<object> |  |
| `pagination` | object |  |
| `snippets` | array<object> |  |
| `updates` | array<object> |  |
| `users` | array<object> |  |

## Native endpoint

Through the native Range API, this operation is `GET /v1/updates` (base URL `https://api.range.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-updates.md) for the provider-specific parameters and requirements.

