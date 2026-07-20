# Enrich.so: List Team Members

Retrieves team members from Enrich.so.

```
GET https://connect.mindcloud.co/v1/universal/enrich/latest/actions/list-team-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Enrich.so `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/enrich/latest/actions/list-team-members?connectionId=$CONNECTION_ID&teamId=team_example" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "team_example"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/enrich/latest/actions/list-team-members?${params}`, {
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
| `teamId` | string | yes | Enrich team ID. Default: `team_example`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "role": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Team member creation timestamp. |
| `email` | string | Team member email address. |
| `id` | string | Team member identifier. |
| `role` | string | Team role such as owner, admin, or member. |
| `status` | string | Team member status. |

## Native endpoint

Through the native Enrich.so API, this operation is `GET /teams/{teamId}/members` (base URL `https://dev.enrich.so/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-team-members.md) for the provider-specific parameters and requirements.

