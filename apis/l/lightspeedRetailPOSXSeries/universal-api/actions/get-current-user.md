# Lightspeed Retail POS (X-Series): Get Current User

Retrieves the current user from Lightspeed Retail POS (X-Series).

```
GET https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightspeed Retail POS (X-Series) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/get-current-user?${params}`, {
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
      "accountType": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "emailVerifiedAt": "2026-05-07T12:00:00.000Z",
      "enabled": true,
      "enabledMfa": true,
      "id": "string",
      "images": {},
      "imageSource": "string",
      "isPrimaryUser": true,
      "permissions": [
        "string"
      ],
      "requirePasswordChange": true,
      "restrictedOutletId": "string",
      "restrictedOutletIds": [
        "string"
      ],
      "roles": [
        {}
      ],
      "rules": {},
      "seenAt": "2026-05-07T12:00:00.000Z",
      "switchId": "string",
      "targetDaily": 1,
      "targetMonthly": 1,
      "targetWeekly": 1,
      "timeUntilDeletion": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "username": "Ava Chen",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountType` | string |  |
| `createdAt` | date |  |
| `deletedAt` | date |  |
| `displayName` | string |  |
| `email` | string |  |
| `emailVerifiedAt` | date |  |
| `enabled` | boolean |  |
| `enabledMfa` | boolean |  |
| `id` | string |  |
| `images` | object |  |
| `imageSource` | string |  |
| `isPrimaryUser` | boolean |  |
| `permissions` | array<string> |  |
| `requirePasswordChange` | boolean |  |
| `restrictedOutletId` | string |  |
| `restrictedOutletIds` | array<string> |  |
| `roles` | array<object> |  |
| `rules` | object |  |
| `seenAt` | date |  |
| `switchId` | string |  |
| `targetDaily` | number |  |
| `targetMonthly` | number |  |
| `targetWeekly` | number |  |
| `timeUntilDeletion` | string |  |
| `updatedAt` | date |  |
| `username` | string |  |
| `version` | number |  |

## Native endpoint

Through the native Lightspeed Retail POS (X-Series) API, this operation is `GET /api/2.0/user` (base URL `https://{{credentials.authorizeRequest.domain_prefix}}.retail.lightspeed.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

