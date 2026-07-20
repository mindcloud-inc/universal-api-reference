# BASIC: Get team invites

Retrieves team invites from BASIC.

```
GET https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-team-invites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BASIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-team-invites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-team-invites?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "created_at": "2026-05-07T12:00:00.000Z",
          "email_or_username": "ava@example.com",
          "expires_at": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "role_name": "Ava Chen",
          "roles": "string",
          "team_id": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].created_at` | date |  |
| `data[].email_or_username` | string |  |
| `data[].expires_at` | date |  |
| `data[].id` | string |  |
| `data[].role_name` | string |  |
| `data[].roles` | string |  |
| `data[].team_id` | string |  |

## Native endpoint

Through the native BASIC API, this operation is `GET /team/{team_id}/invite` (base URL `https://api.basic.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team-invites.md) for the provider-specific parameters and requirements.

