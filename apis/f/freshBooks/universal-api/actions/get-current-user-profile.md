# FreshBooks: Get Current User Profile

Retrieves the current user profile from FreshBooks.

```
GET https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/get-current-user-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FreshBooks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/get-current-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/get-current-user-profile?${params}`, {
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
      "businessMemberships": [
        {}
      ],
      "businessStatuses": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "groups": [
        {}
      ],
      "id": 1,
      "identityId": 1,
      "identityOrigin": "string",
      "identityUuid": "string",
      "integrations": {},
      "language": "string",
      "lastName": "Chen",
      "links": {},
      "otpDeliveryMethod": "string",
      "otpRequiredForLogin": true,
      "permissions": {},
      "profile": {},
      "roles": [
        {}
      ],
      "setupComplete": true,
      "subscriptionStatuses": {},
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `businessMemberships` | array<object> | Business membership records for the authenticated user. |
| `businessStatuses` | object | Business status by FreshBooks account. |
| `createdAt` | date | FreshBooks account creation timestamp. |
| `email` | string | Primary email address for the authenticated user. |
| `firstName` | string | User first name. |
| `groups` | array<object> | Business group memberships for the authenticated user. |
| `id` | number | FreshBooks identity ID. |
| `identityId` | number | Canonical identity identifier for the authenticated user. |
| `identityOrigin` | string | FreshBooks origin for the identity record. |
| `identityUuid` | string | UUID for the authenticated FreshBooks identity. |
| `integrations` | object | Connected integration details keyed by provider. |
| `language` | string | Preferred language code. |
| `lastName` | string | User last name. |
| `links` | object | FreshBooks API links related to the current identity. |
| `otpDeliveryMethod` | string | Delivery method for one-time passwords. |
| `otpRequiredForLogin` | boolean | Whether one-time password login is required. |
| `permissions` | object | Feature and entitlement map by FreshBooks account. |
| `profile` | object | Expanded profile details for the authenticated user. |
| `roles` | array<object> | Role assignments for the authenticated user. |
| `setupComplete` | boolean | Whether account setup is complete. |
| `subscriptionStatuses` | object | Subscription status by FreshBooks account. |
| `timezone` | string | Preferred timezone for the authenticated user. |

## Native endpoint

Through the native FreshBooks API, this operation is `GET /auth/api/v1/users/me` (base URL `https://api.freshbooks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user-profile.md) for the provider-specific parameters and requirements.

