# Layer4: List Wallets

Retrieves wallets from Layer4.

```
GET https://connect.mindcloud.co/v1/universal/layer4/latest/actions/list-wallets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Layer4 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/layer4/latest/actions/list-wallets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/layer4/latest/actions/list-wallets?${params}`, {
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
| `status[]` | array<string> | no | Filter wallets by one or more statuses: ACTIVE, PENDING, or DECLINED. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "user": {},
      "workspace": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | When the wallet was created. |
| `id` | string | The unique wallet identifier. |
| `name` | string | The wallet name assigned by the workspace owner. |
| `status` | string | The current wallet connection status. |
| `updatedAt` | date | When the wallet was last updated. |
| `user` | object | Connected user details for the wallet. |
| `workspace` | object | Workspace details for the wallet. |

## Native endpoint

Through the native Layer4 API, this operation is `GET /api/v1/wallets` (base URL `https://www.layer4.app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-wallets.md) for the provider-specific parameters and requirements.

