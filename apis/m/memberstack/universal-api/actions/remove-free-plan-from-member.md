# Memberstack: Remove Free Plan from Member



```
DELETE https://connect.mindcloud.co/v1/universal/memberstack/latest/actions/remove-free-plan-from-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Memberstack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/memberstack/latest/actions/remove-free-plan-from-member?connectionId=$CONNECTION_ID&id=string&planId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "planId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/memberstack/latest/actions/remove-free-plan-from-member?${params}`, {
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
| `id` | string | yes | Member ID (mem_...) to remove plan from. |
| `planId` | string | yes | Plan ID to remove from the member. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "auth": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customFields": {},
      "id": "string",
      "lastLogin": "2026-05-07T12:00:00.000Z",
      "loginRedirect": "string",
      "metaData": {},
      "permissions": [
        "string"
      ],
      "planConnections": [
        {}
      ],
      "profileImage": "string",
      "stripeCustomerId": "string",
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auth` | object |  |
| `createdAt` | date |  |
| `customFields` | object |  |
| `id` | string |  |
| `lastLogin` | date |  |
| `loginRedirect` | string |  |
| `metaData` | object |  |
| `permissions` | array<string> |  |
| `planConnections` | array<object> |  |
| `profileImage` | string |  |
| `stripeCustomerId` | string |  |
| `verified` | boolean |  |

## Native endpoint

Through the native Memberstack API, this operation is `POST /members/:id/remove-plan` (base URL `https://admin.memberstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-free-plan-from-member.md) for the provider-specific parameters and requirements.

