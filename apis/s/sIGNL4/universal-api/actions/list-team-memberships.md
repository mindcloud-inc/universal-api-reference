# SIGNL4: List Team Memberships

Retrieves team memberships from SIGNL4.

```
GET https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/list-team-memberships
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SIGNL4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/list-team-memberships?connectionId=$CONNECTION_ID&teamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/list-team-memberships?${params}`, {
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
| `teamId` | string | yes | Team ID of team you want to access. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "mailAddress": "string",
      "memberSince": "2026-05-07T12:00:00.000Z",
      "roleId": "string",
      "status": 1,
      "teamId": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `mailAddress` | string |  |
| `memberSince` | date |  |
| `roleId` | string |  |
| `status` | number |  |
| `teamId` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native SIGNL4 API, this operation is `GET /v2/teams/{teamId}/memberships` (base URL `https://connect.signl4.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-team-memberships.md) for the provider-specific parameters and requirements.

