# Lightspeed Retail POS (X-Series): Get User

Retrieves a user from Lightspeed Retail POS (X-Series).

```
GET https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightspeed Retail POS (X-Series) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/get-user?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/get-user?${params}`, {
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
| `userId` | string | yes | The Lightspeed user ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountType": "string",
      "createdAt": "string",
      "deletedAt": "string",
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "emailVerifiedAt": "ava@example.com",
      "enabled": "string",
      "enabledMfa": "string",
      "id": "string",
      "images": "string",
      "imageSource": "string",
      "isPrimaryUser": "string",
      "permissions": "string",
      "requirePasswordChange": "string",
      "restrictedOutletId": "string",
      "restrictedOutletIds": "string",
      "roles": "string",
      "rules": "string",
      "seenAt": "string",
      "switchId": "string",
      "targetDaily": "string",
      "targetMonthly": "string",
      "targetWeekly": "string",
      "timeUntilDeletion": "string",
      "updatedAt": "string",
      "username": "Ava Chen",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountType` | string |  |
| `createdAt` | string |  |
| `deletedAt` | string |  |
| `displayName` | string |  |
| `email` | string |  |
| `emailVerifiedAt` | string |  |
| `enabled` | string |  |
| `enabledMfa` | string |  |
| `id` | string |  |
| `images` | string |  |
| `imageSource` | string |  |
| `isPrimaryUser` | string |  |
| `permissions` | string |  |
| `requirePasswordChange` | string |  |
| `restrictedOutletId` | string |  |
| `restrictedOutletIds` | string |  |
| `roles` | string |  |
| `rules` | string |  |
| `seenAt` | string |  |
| `switchId` | string |  |
| `targetDaily` | string |  |
| `targetMonthly` | string |  |
| `targetWeekly` | string |  |
| `timeUntilDeletion` | string |  |
| `updatedAt` | string |  |
| `username` | string |  |
| `version` | string |  |

## Native endpoint

Through the native Lightspeed Retail POS (X-Series) API, this operation is `GET /api/2.0/users/:user_id` (base URL `https://{{credentials.authorizeRequest.domain_prefix}}.retail.lightspeed.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

