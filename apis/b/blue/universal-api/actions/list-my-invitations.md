# Blue: List My Invitations

Retrieves your pending invitations from Blue.

```
GET https://connect.mindcloud.co/v1/universal/blue/latest/actions/list-my-invitations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blue/latest/actions/list-my-invitations?connectionId=$CONNECTION_ID&companyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blue/latest/actions/list-my-invitations?${params}`, {
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
| `companyId` | string | yes | Blue company node ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessLevel": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "expiredAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessLevel` | string |  |
| `createdAt` | date |  |
| `email` | string |  |
| `expiredAt` | date |  |
| `id` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Blue API, this operation is `POST /graphql` (base URL `https://api.blue.cc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-my-invitations.md) for the provider-specific parameters and requirements.

