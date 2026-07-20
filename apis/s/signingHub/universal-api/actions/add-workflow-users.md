# SigningHub: Add Workflow Users

Adds users to a workflow in SigningHub.

```
POST https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/add-workflow-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigningHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/add-workflow-users" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "packageId": "11191534",
  "users[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/add-workflow-users', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "packageId": "11191534",
    "users[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `packageId` | number | yes | SigningHub package ID, which the recipients are to be added to. Example: `11191534`. |
| `users[]` | array<object> | yes | One or more workflow users to add. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email_language_code": "ava@example.com",
      "guest_user": true,
      "permission": {},
      "reminder": {},
      "signing_order": 1,
      "user_email": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email_language_code` | string |  |
| `guest_user` | boolean |  |
| `permission` | object |  |
| `reminder` | object |  |
| `signing_order` | number |  |
| `user_email` | string |  |

## Native endpoint

Through the native SigningHub API, this operation is `POST /v4/packages/:packageId/workflow/users` (base URL `https://api.signinghub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-workflow-users.md) for the provider-specific parameters and requirements.

