# SignWell: Get Credentials

Retrieves account and user details from SignWell.

```
GET https://connect.mindcloud.co/v1/universal/signWell/latest/actions/get-credentials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignWell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signWell/latest/actions/get-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signWell/latest/actions/get-credentials?${params}`, {
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
      "account": {
        "activeTemplates": 1,
        "activeUsers": [
          {
            "email": "ava@example.com",
            "hasGoogleRegistration": true,
            "id": "string",
            "name": "Ava Chen"
          }
        ],
        "canCreateCompletionDocument": true,
        "canCreateTemplate": true,
        "canCreateTrackingDocument": true,
        "id": "string",
        "name": "Ava Chen",
        "planTier": "string"
      },
      "archived": true,
      "contact": {
        "altPhoneNumber": {},
        "archived": true,
        "companyName": {},
        "email": "ava@example.com",
        "id": "string",
        "initials": "string",
        "name": "Ava Chen",
        "phoneNumber": {},
        "website": {}
      },
      "id": "string",
      "role": "string",
      "user": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "hasGoogleRegistration": true,
        "id": "string",
        "name": "Ava Chen"
      },
      "workspace": {
        "activeTemplates": 1,
        "activeUsers": [
          {
            "email": "ava@example.com",
            "hasGoogleRegistration": true,
            "id": "string",
            "name": "Ava Chen"
          }
        ],
        "canCreateCompletionDocument": true,
        "canCreateTemplate": true,
        "canCreateTrackingDocument": true,
        "id": "string",
        "name": "Ava Chen",
        "planTier": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account.activeTemplates` | number |  |
| `account.activeUsers[].email` | string |  |
| `account.activeUsers[].hasGoogleRegistration` | boolean |  |
| `account.activeUsers[].id` | string |  |
| `account.activeUsers[].name` | string |  |
| `account.canCreateCompletionDocument` | boolean |  |
| `account.canCreateTemplate` | boolean |  |
| `account.canCreateTrackingDocument` | boolean |  |
| `account.id` | string |  |
| `account.name` | string |  |
| `account.planTier` | string |  |
| `archived` | boolean |  |
| `contact.altPhoneNumber` | object |  |
| `contact.archived` | boolean |  |
| `contact.companyName` | object |  |
| `contact.email` | string |  |
| `contact.id` | string |  |
| `contact.initials` | string |  |
| `contact.name` | string |  |
| `contact.phoneNumber` | object |  |
| `contact.website` | object |  |
| `id` | string |  |
| `role` | string |  |
| `user.email` | string |  |
| `user.firstName` | string |  |
| `user.hasGoogleRegistration` | boolean |  |
| `user.id` | string |  |
| `user.name` | string |  |
| `workspace.activeTemplates` | number |  |
| `workspace.activeUsers[].email` | string |  |
| `workspace.activeUsers[].hasGoogleRegistration` | boolean |  |
| `workspace.activeUsers[].id` | string |  |
| `workspace.activeUsers[].name` | string |  |
| `workspace.canCreateCompletionDocument` | boolean |  |
| `workspace.canCreateTemplate` | boolean |  |
| `workspace.canCreateTrackingDocument` | boolean |  |
| `workspace.id` | string |  |
| `workspace.name` | string |  |
| `workspace.planTier` | string |  |

## Native endpoint

Through the native SignWell API, this operation is `GET /me` (base URL `https://www.signwell.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-credentials.md) for the provider-specific parameters and requirements.

