# Salesflare: Get Current User



```
GET https://connect.mindcloud.co/v1/universal/salesflare/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesflare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesflare/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesflare/latest/actions/get-current-user?${params}`, {
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
      "creationDate": "2026-05-07T12:00:00.000Z",
      "dataSources": [
        {}
      ],
      "disabled": true,
      "domain": "string",
      "email": "ava@example.com",
      "firstname": "Ava",
      "flags": [
        {}
      ],
      "id": 1,
      "intercomHash": "string",
      "isAdmin": true,
      "language": "string",
      "lastname": "Chen",
      "modificationDate": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "picture": "string",
      "role": {},
      "syncStatus": "string",
      "team": {},
      "trialExpired": true,
      "trialExpiryDate": "2026-05-07T12:00:00.000Z",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creationDate` | date | When the user record was created. |
| `dataSources` | array<object> | Connected data sources for the user account. |
| `disabled` | boolean | Whether the user account is disabled. |
| `domain` | string | The account domain associated with the user. |
| `email` | string | The user's primary email address. |
| `firstname` | string | The user's first name. |
| `flags` | array<object> | Feature flags and state for the user account. |
| `id` | number | The Salesflare user ID. |
| `intercomHash` | string | The Intercom hash associated with the user. |
| `isAdmin` | boolean | Whether the user is a Salesflare admin. |
| `language` | string | The user's language preference. |
| `lastname` | string | The user's last name. |
| `modificationDate` | date | When the user record was last modified. |
| `name` | string | The full display name. |
| `picture` | string | The avatar image URL. |
| `role` | object | The user's Salesflare role information. |
| `syncStatus` | string | The current sync state for the user account. |
| `team` | object | The Salesflare team details for the current user. |
| `trialExpired` | boolean | Whether the Salesflare trial has expired. |
| `trialExpiryDate` | date | When the Salesflare trial expires. |
| `type` | string | The Salesflare principal type. |

## Native endpoint

Through the native Salesflare API, this operation is `GET me` (base URL `https://api.salesflare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

