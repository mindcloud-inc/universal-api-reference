# BASIC: Get team members

Retrieves team members from BASIC.

```
GET https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-team-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BASIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-team-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-team-members?${params}`, {
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
          "account_id": "string",
          "created_at": "2026-05-07T12:00:00.000Z",
          "role_name": "Ava Chen",
          "roles": "string"
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
| `data[].account_id` | string |  |
| `data[].created_at` | date |  |
| `data[].role_name` | string |  |
| `data[].roles` | string |  |

## Native endpoint

Through the native BASIC API, this operation is `GET /team/{team_id}/member` (base URL `https://api.basic.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team-members.md) for the provider-specific parameters and requirements.

