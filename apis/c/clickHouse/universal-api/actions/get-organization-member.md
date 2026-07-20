# ClickHouse: Get Organization Member



```
GET https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/get-organization-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickHouse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/get-organization-member?connectionId=$CONNECTION_ID&organizationId=string&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "string",
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/get-organization-member?${params}`, {
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
| `organizationId` | string | yes | ID of the requested organization. |
| `userId` | string | yes | ID of the requested organization member. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedRoles": [
        {}
      ],
      "email": "ava@example.com",
      "joinedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "role": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedRoles` | array<object> | Assigned role objects. |
| `email` | string | Member email address. |
| `joinedAt` | date | Member join timestamp. |
| `name` | string | Member name. |
| `role` | string | Member role. |
| `userId` | string | Organization member user ID. |

## Native endpoint

Through the native ClickHouse API, this operation is `GET /v1/organizations/[:organizationId]/members/[:userId]` (base URL `https://api.clickhouse.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-member.md) for the provider-specific parameters and requirements.

