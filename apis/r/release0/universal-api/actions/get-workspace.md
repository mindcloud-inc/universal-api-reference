# Release0: Get Workspace

Retrieves a workspace from Release0.

```
GET https://connect.mindcloud.co/v1/universal/release0/latest/actions/get-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Release0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/release0/latest/actions/get-workspace?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/release0/latest/actions/get-workspace?${params}`, {
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
| `workspaceId` | string | yes | The workspace ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addons": [
        "string"
      ],
      "billingCycleStart": 1,
      "chatUsage": 1,
      "createdAt": "string",
      "extras": [
        "string"
      ],
      "icon": "string",
      "id": "string",
      "isPastDue": true,
      "isQuarantined": true,
      "isSuspended": true,
      "isVerified": true,
      "lastActivityAt": "string",
      "name": "Ava Chen",
      "paymentFailedAt": "string",
      "plan": "string",
      "redeemedCoupons": "string",
      "slug": "string",
      "stripeConnectId": "string",
      "stripeId": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addons` | array<string> |  |
| `billingCycleStart` | number |  |
| `chatUsage` | number |  |
| `createdAt` | string |  |
| `extras` | array<string> |  |
| `icon` | string |  |
| `id` | string |  |
| `isPastDue` | boolean |  |
| `isQuarantined` | boolean |  |
| `isSuspended` | boolean |  |
| `isVerified` | boolean |  |
| `lastActivityAt` | string |  |
| `name` | string |  |
| `paymentFailedAt` | string |  |
| `plan` | string |  |
| `redeemedCoupons` | string |  |
| `slug` | string |  |
| `stripeConnectId` | string |  |
| `stripeId` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Release0 API, this operation is `GET /v1/workspaces/:workspaceId` (base URL `https://release0.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace.md) for the provider-specific parameters and requirements.

