# Kite Suite: Get User By workspace ID



```
GET https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-user-by-workspace-idget-api-v1-user-workspace-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-user-by-workspace-idget-api-v1-user-workspace-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-user-by-workspace-idget-api-v1-user-workspace-id?${params}`, {
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
| `id` | string | yes | workspace ID |

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

Through the native Kite Suite API, this operation is `GET /api/v1/user/workspace/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-by-workspace-idget-api-v1-user-workspace-id.md) for the provider-specific parameters and requirements.

