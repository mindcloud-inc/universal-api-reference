# Memberstack: Get Member



```
GET https://connect.mindcloud.co/v1/universal/memberstack/latest/actions/get-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Memberstack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/memberstack/latest/actions/get-member?connectionId=$CONNECTION_ID&idOrEmail=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idOrEmail": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/memberstack/latest/actions/get-member?${params}`, {
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
| `idOrEmail` | string | yes | Member ID (mem_...) or URL-encoded member email. |

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

Through the native Memberstack API, this operation is `GET /members/:id_or_email` (base URL `https://admin.memberstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-member.md) for the provider-specific parameters and requirements.

