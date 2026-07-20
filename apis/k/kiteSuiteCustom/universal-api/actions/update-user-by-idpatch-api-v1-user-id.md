# Kite Suite: Update User By ID



```
PUT https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-user-by-idpatch-api-v1-user-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-user-by-idpatch-api-v1-user-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "body": {},
  "fullName": "Ava Chen",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-user-by-idpatch-api-v1-user-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "body": {},
    "fullName": "Ava Chen",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | user ID |
| `body` | object | yes | Request body |
| `fullName` | string | yes |  |
| `email` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar": "string",
      "department": "string",
      "email": "ava@example.com",
      "fullName": "Ava Chen",
      "id": "string",
      "isDeleted": true,
      "isOnline": true,
      "jobTitle": "string",
      "otp": "string",
      "password": [
        "string"
      ],
      "selectedWorkspace": "string",
      "settings": {},
      "status": "string",
      "tenant": "string",
      "verifiedPasswordKey": "string",
      "workspaces": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | string | filename. |
| `department` | string | department of user |
| `email` | string | email address of user. |
| `fullName` | string | The name of the user. |
| `id` | string | The auto-generated id of the user. |
| `isDeleted` | boolean | user availablity status. |
| `isOnline` | boolean | username of user. |
| `jobTitle` | string | job title of user |
| `otp` | string | otp for two step verification. |
| `password` | array | passwords of user. |
| `selectedWorkspace` | string | selected workspace. |
| `settings` | object |  |
| `status` | string | status of user (active,away,do not disturb, invisible). |
| `tenant` | string | tanant ID of user |
| `verifiedPasswordKey` | string | two steph otp of user |
| `workspaces` | array |  |

## Native endpoint

Through the native Kite Suite API, this operation is `PATCH /api/v1/user/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user-by-idpatch-api-v1-user-id.md) for the provider-specific parameters and requirements.

